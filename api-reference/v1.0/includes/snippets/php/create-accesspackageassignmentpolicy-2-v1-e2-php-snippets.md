---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\AccessPackageAssignmentPolicy;
use Microsoft\Graph\Generated\Models\AllowedTargetScope;
use Microsoft\Graph\Generated\Models\SubjectSet;
use Microsoft\Graph\Generated\Models\ExpirationPattern;
use Microsoft\Graph\Generated\Models\ExpirationPatternType;
use Microsoft\Graph\Generated\Models\AccessPackageAssignmentRequestorSettings;
use Microsoft\Graph\Generated\Models\AccessPackageAssignmentApprovalSettings;
use Microsoft\Graph\Generated\Models\AccessPackageApprovalStage;
use Microsoft\Graph\Generated\Models\InternalSponsors;
use Microsoft\Graph\Generated\Models\SingleUser;
use Microsoft\Graph\Generated\Models\GroupMembers;
use Microsoft\Graph\Generated\Models\AccessPackageAssignmentReviewSettings;
use Microsoft\Graph\Generated\Models\AccessReviewExpirationBehavior;
use Microsoft\Graph\Generated\Models\EntitlementManagementSchedule;
use Microsoft\Graph\Generated\Models\PatternedRecurrence;
use Microsoft\Graph\Generated\Models\RecurrencePattern;
use Microsoft\Graph\Generated\Models\RecurrencePatternType;
use Microsoft\Graph\Generated\Models\DayOfWeek;
use Microsoft\Graph\Generated\Models\RecurrenceRange;
use Microsoft\Graph\Generated\Models\RecurrenceRangeType;
use Microsoft\Graph\Generated\Models\AccessPackage;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AccessPackageAssignmentPolicy();
$requestBody->setDisplayName('policy for external access requests');
$requestBody->setDescription('policy for users from connected organizations to request access, with two stages of approval.');
$requestBody->setAllowedTargetScope(new AllowedTargetScope('allConfiguredConnectedOrganizationUsers'));
$requestBody->setSpecificAllowedTargets([	]);
$expiration = new ExpirationPattern();
$expiration->setType(new ExpirationPatternType('noExpiration'));
$requestBody->setExpiration($expiration);
$requestorSettings = new AccessPackageAssignmentRequestorSettings();
$requestorSettings->setEnableTargetsToSelfAddAccess(true);
$requestorSettings->setEnableTargetsToSelfUpdateAccess(true);
$requestorSettings->setEnableTargetsToSelfRemoveAccess(true);
$requestorSettings->setAllowCustomAssignmentSchedule(false);
$requestorSettings->setEnableOnBehalfRequestorsToAddAccess(false);
$requestorSettings->setEnableOnBehalfRequestorsToUpdateAccess(false);
$requestorSettings->setEnableOnBehalfRequestorsToRemoveAccess(false);
$requestorSettings->setOnBehalfRequestors([	]);
$requestBody->setRequestorSettings($requestorSettings);
$requestApprovalSettings = new AccessPackageAssignmentApprovalSettings();
$requestApprovalSettings->setIsApprovalRequiredForAdd(true);
$requestApprovalSettings->setIsApprovalRequiredForUpdate(false);
$stagesAccessPackageApprovalStage1 = new AccessPackageApprovalStage();
$stagesAccessPackageApprovalStage1->setDurationBeforeAutomaticDenial(new \DateInterval('P14D'));
$stagesAccessPackageApprovalStage1->setIsApproverJustificationRequired(false);
$stagesAccessPackageApprovalStage1->setIsEscalationEnabled(false);
$stagesAccessPackageApprovalStage1->setDurationBeforeEscalation(new \DateInterval('PT0S'));
$primaryApproversSubjectSet1 = new InternalSponsors();
$primaryApproversSubjectSet1->setOdataType('#microsoft.graph.internalSponsors');
$primaryApproversArray []= $primaryApproversSubjectSet1;
$stagesAccessPackageApprovalStage1->setPrimaryApprovers($primaryApproversArray);

$fallbackPrimaryApproversSubjectSet1 = new SingleUser();
$fallbackPrimaryApproversSubjectSet1->setOdataType('#microsoft.graph.singleUser');
$fallbackPrimaryApproversSubjectSet1->setUserId('7deff43e-1f17-44ef-9e5f-d516b0ba11d4');
$fallbackPrimaryApproversArray []= $fallbackPrimaryApproversSubjectSet1;
$fallbackPrimaryApproversSubjectSet2 = new GroupMembers();
$fallbackPrimaryApproversSubjectSet2->setOdataType('#microsoft.graph.groupMembers');
$fallbackPrimaryApproversSubjectSet2->setGroupId('1623f912-5e86-41c2-af47-39dd67582b66');
$fallbackPrimaryApproversArray []= $fallbackPrimaryApproversSubjectSet2;
$stagesAccessPackageApprovalStage1->setFallbackPrimaryApprovers($fallbackPrimaryApproversArray);

$stagesAccessPackageApprovalStage1->setEscalationApprovers([]);
$stagesAccessPackageApprovalStage1->setFallbackEscalationApprovers([]);
$stagesArray []= $stagesAccessPackageApprovalStage1;
$stagesAccessPackageApprovalStage2 = new AccessPackageApprovalStage();
$stagesAccessPackageApprovalStage2->setDurationBeforeAutomaticDenial(new \DateInterval('P14D'));
$stagesAccessPackageApprovalStage2->setIsApproverJustificationRequired(false);
$stagesAccessPackageApprovalStage2->setIsEscalationEnabled(false);
$stagesAccessPackageApprovalStage2->setDurationBeforeEscalation(new \DateInterval('PT0S'));
$stagesAccessPackageApprovalStage2->setPrimaryApprovers([]);
$fallbackPrimaryApproversSubjectSet1 = new SingleUser();
$fallbackPrimaryApproversSubjectSet1->setOdataType('#microsoft.graph.singleUser');
$fallbackPrimaryApproversSubjectSet1->setUserId('46184453-e63b-4f20-86c2-c557ed5d5df9');
$fallbackPrimaryApproversArray []= $fallbackPrimaryApproversSubjectSet1;
$fallbackPrimaryApproversSubjectSet2 = new GroupMembers();
$fallbackPrimaryApproversSubjectSet2->setOdataType('#microsoft.graph.groupMembers');
$fallbackPrimaryApproversSubjectSet2->setGroupId('1623f912-5e86-41c2-af47-39dd67582b66');
$fallbackPrimaryApproversArray []= $fallbackPrimaryApproversSubjectSet2;
$stagesAccessPackageApprovalStage2->setFallbackPrimaryApprovers($fallbackPrimaryApproversArray);

$stagesAccessPackageApprovalStage2->setEscalationApprovers([]);
$stagesAccessPackageApprovalStage2->setFallbackEscalationApprovers([]);
$stagesArray []= $stagesAccessPackageApprovalStage2;
$requestApprovalSettings->setStages($stagesArray);

$requestBody->setRequestApprovalSettings($requestApprovalSettings);
$reviewSettings = new AccessPackageAssignmentReviewSettings();
$reviewSettings->setIsEnabled(true);
$reviewSettings->setExpirationBehavior(new AccessReviewExpirationBehavior('keepAccess'));
$reviewSettings->setIsRecommendationEnabled(true);
$reviewSettings->setIsReviewerJustificationRequired(true);
$reviewSettings->setIsSelfReview(false);
$reviewSettingsSchedule = new EntitlementManagementSchedule();
$reviewSettingsSchedule->setStartDateTime(new \DateTime('2022-07-02T06:59:59.998Z'));
$reviewSettingsScheduleExpiration = new ExpirationPattern();
$reviewSettingsScheduleExpiration->setDuration(new \DateInterval('P14D'));
$reviewSettingsScheduleExpiration->setType(new ExpirationPatternType('afterDuration'));
$reviewSettingsSchedule->setExpiration($reviewSettingsScheduleExpiration);
$reviewSettingsScheduleRecurrence = new PatternedRecurrence();
$reviewSettingsScheduleRecurrencePattern = new RecurrencePattern();
$reviewSettingsScheduleRecurrencePattern->setType(new RecurrencePatternType('absoluteMonthly'));
$reviewSettingsScheduleRecurrencePattern->setInterval(3);
$reviewSettingsScheduleRecurrencePattern->setMonth(0);
$reviewSettingsScheduleRecurrencePattern->setDayOfMonth(0);
$reviewSettingsScheduleRecurrencePattern->setDaysOfWeek([]);
$reviewSettingsScheduleRecurrence->setPattern($reviewSettingsScheduleRecurrencePattern);
$reviewSettingsScheduleRecurrenceRange = new RecurrenceRange();
$reviewSettingsScheduleRecurrenceRange->setType(new RecurrenceRangeType('noEnd'));
$reviewSettingsScheduleRecurrenceRange->setNumberOfOccurrences(0);
$reviewSettingsScheduleRecurrence->setRange($reviewSettingsScheduleRecurrenceRange);
$reviewSettingsSchedule->setRecurrence($reviewSettingsScheduleRecurrence);
$reviewSettings->setSchedule($reviewSettingsSchedule);
$primaryReviewersSubjectSet1 = new GroupMembers();
$primaryReviewersSubjectSet1->setOdataType('#microsoft.graph.groupMembers');
$primaryReviewersSubjectSet1->setGroupId('1623f912-5e86-41c2-af47-39dd67582b66');
$primaryReviewersArray []= $primaryReviewersSubjectSet1;
$reviewSettings->setPrimaryReviewers($primaryReviewersArray);

$reviewSettings->setFallbackReviewers([]);
$requestBody->setReviewSettings($reviewSettings);
$accessPackage = new AccessPackage();
$accessPackage->setId('a2e1ca1e-4e56-47d2-9daa-e2ba8d12a82b');
$requestBody->setAccessPackage($accessPackage);

$result = $graphServiceClient->identityGovernance()->entitlementManagement()->assignmentPolicies()->post($requestBody)->wait();

```