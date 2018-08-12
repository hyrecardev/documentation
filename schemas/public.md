# Schema Types

<details>
  <summary><strong>Table of Contents</strong></summary>

  * [Query](#query)
  * [Mutation](#mutation)
  * [Objects](#objects)
    * [Accident](#accident)
    * [AddRemoveCarPhotoPayload](#addremovecarphotopayload)
    * [Admin](#admin)
    * [AdminNote](#adminnote)
    * [AdminNoteConnection](#adminnoteconnection)
    * [AdminNoteEdge](#adminnoteedge)
    * [AggregateAdminNote](#aggregateadminnote)
    * [AggregateCar](#aggregatecar)
    * [AggregateClaim](#aggregateclaim)
    * [AggregateInsurance](#aggregateinsurance)
    * [AggregateRating](#aggregaterating)
    * [AggregateRental](#aggregaterental)
    * [ApproveRejectBookingPayload](#approverejectbookingpayload)
    * [Auth0Details](#auth0details)
    * [BackgroundCheck](#backgroundcheck)
    * [BackgroundCheckMissingInfo](#backgroundcheckmissinginfo)
    * [BackgroundCheckPayment](#backgroundcheckpayment)
    * [Car](#car)
    * [CarConnection](#carconnection)
    * [CarDocument](#cardocument)
    * [CarEdge](#caredge)
    * [CarLocation](#carlocation)
    * [CarMissingInfo](#carmissinginfo)
    * [CarPhoto](#carphoto)
    * [CarPriceBreakdown](#carpricebreakdown)
    * [CarRatingsMeta](#carratingsmeta)
    * [Claim](#claim)
    * [ClaimConnection](#claimconnection)
    * [ClaimEdge](#claimedge)
    * [ClaimInvoice](#claiminvoice)
    * [ClaimInvoiceItem](#claiminvoiceitem)
    * [ClaimInvoiceOverview](#claiminvoiceoverview)
    * [ClaimPayment](#claimpayment)
    * [ClaimStatement](#claimstatement)
    * [ConfirmDropoffPayload](#confirmdropoffpayload)
    * [ConfirmPickupPayload](#confirmpickuppayload)
    * [Coupon](#coupon)
    * [CreateClaimEvidencePayload](#createclaimevidencepayload)
    * [Deposit](#deposit)
    * [Driver](#driver)
    * [DriverClaimsMeta](#driverclaimsmeta)
    * [DriverLegalInfo](#driverlegalinfo)
    * [DriverRatingsMeta](#driverratingsmeta)
    * [Evidence](#evidence)
    * [ExtendRentalPayload](#extendrentalpayload)
    * [FactOfLoss](#factofloss)
    * [File](#file)
    * [GeoState](#geostate)
    * [Incidental](#incidental)
    * [Insurance](#insurance)
    * [InsuranceConnection](#insuranceconnection)
    * [InsuranceEdge](#insuranceedge)
    * [InvolvedParty](#involvedparty)
    * [ListCarPayload](#listcarpayload)
    * [Location](#location)
    * [LoginUserPayload](#loginuserpayload)
    * [Owner](#owner)
    * [PageInfo](#pageinfo)
    * [PaymentAccount](#paymentaccount)
    * [PayoutAccount](#payoutaccount)
    * [PoliceReport](#policereport)
    * [PostInsurance](#postinsurance)
    * [PreInsurance](#preinsurance)
    * [PreInsurancePhoto](#preinsurancephoto)
    * [RateDriverPayload](#ratedriverpayload)
    * [Rating](#rating)
    * [RatingConnection](#ratingconnection)
    * [RatingEdge](#ratingedge)
    * [Rental](#rental)
    * [RentalConnection](#rentalconnection)
    * [RentalEdge](#rentaledge)
    * [RentalLateFeePayment](#rentallatefeepayment)
    * [RentalOverview](#rentaloverview)
    * [RentalPayment](#rentalpayment)
    * [RentalPeriod](#rentalperiod)
    * [RequestBookingPayload](#requestbookingpayload)
    * [StartBackgroundCheckPayload](#startbackgroundcheckpayload)
    * [StripeCharge](#stripecharge)
    * [StripePaymentInformation](#stripepaymentinformation)
    * [StripePaymentSource](#stripepaymentsource)
    * [StripePayoutBank](#stripepayoutbank)
    * [StripePayoutInformation](#stripepayoutinformation)
    * [TncUsageDetails](#tncusagedetails)
    * [ToggleListingPayload](#togglelistingpayload)
    * [ToggleRentalExtensionPayload](#togglerentalextensionpayload)
    * [UpdateCarPayload](#updatecarpayload)
    * [UpdatePaymentInfoPayload](#updatepaymentinfopayload)
    * [UpdatePayoutInfoPayload](#updatepayoutinfopayload)
    * [UpdateProfilePayload](#updateprofilepayload)
    * [UpdateProfilePhotoPayload](#updateprofilephotopayload)
    * [UploadCarDocumentPayload](#uploadcardocumentpayload)
    * [User](#user)
    * [UserLocation](#userlocation)
    * [ValidateVin](#validatevin)
    * [Viewer](#viewer)
  * [Enums](#enums)
    * [AdminNoteOrderByInput](#adminnoteorderbyinput)
    * [AdminPermissions](#adminpermissions)
    * [BackgroundCheckPaymentOrderByInput](#backgroundcheckpaymentorderbyinput)
    * [CarDocumentOrderByInput](#cardocumentorderbyinput)
    * [CarDocumentTypeEnum](#cardocumenttypeenum)
    * [CarOrderByInput](#carorderbyinput)
    * [CarPhotoOrderByInput](#carphotoorderbyinput)
    * [CarStatusEnum](#carstatusenum)
    * [CheckrStatusEnum](#checkrstatusenum)
    * [ClaimInvoiceOrderByInput](#claiminvoiceorderbyinput)
    * [ClaimInvoiceStatus](#claiminvoicestatus)
    * [ClaimOrderByInput](#claimorderbyinput)
    * [ClaimPaidByParty](#claimpaidbyparty)
    * [ClaimPaymentOrderByInput](#claimpaymentorderbyinput)
    * [ClaimPaymentPlanManager](#claimpaymentplanmanager)
    * [ClaimPaymentPlanPeriod](#claimpaymentplanperiod)
    * [ClaimPaymentPlanStatus](#claimpaymentplanstatus)
    * [ClaimReportedBy](#claimreportedby)
    * [ClaimStatus](#claimstatus)
    * [DamageLocation](#damagelocation)
    * [DamageType](#damagetype)
    * [DepositOrderByInput](#depositorderbyinput)
    * [DriverVerificationStatusEnum](#driververificationstatusenum)
    * [EvidenceFileType](#evidencefiletype)
    * [EvidenceOrderByInput](#evidenceorderbyinput)
    * [EvidenceType](#evidencetype)
    * [FileTypeEnum](#filetypeenum)
    * [IncidentalOrderByInput](#incidentalorderbyinput)
    * [IncidentalType](#incidentaltype)
    * [InsuranceOrderByInput](#insuranceorderbyinput)
    * [InsuranceStatus](#insurancestatus)
    * [InvolvedPartyType](#involvedpartytype)
    * [MarketStatusEnum](#marketstatusenum)
    * [OffersSortByEnum](#offerssortbyenum)
    * [PaymentAccountOrderByInput](#paymentaccountorderbyinput)
    * [PaymentAccountStatusEnum](#paymentaccountstatusenum)
    * [PaymentProviderTypeEnum](#paymentprovidertypeenum)
    * [PayoutAccountOrderByInput](#payoutaccountorderbyinput)
    * [PreInsurancePhotoOrderByInput](#preinsurancephotoorderbyinput)
    * [PreInsurancePhotoTypeEnum](#preinsurancephototypeenum)
    * [RatingOrderByInput](#ratingorderbyinput)
    * [RatingType](#ratingtype)
    * [RentalCancellationTypeEnum](#rentalcancellationtypeenum)
    * [RentalLateFeePaymentOrderByInput](#rentallatefeepaymentorderbyinput)
    * [RentalOrderByInput](#rentalorderbyinput)
    * [RentalPaymentOrderByInput](#rentalpaymentorderbyinput)
    * [RentalPeriodOrderByInput](#rentalperiodorderbyinput)
    * [RentalPeriodTypeEnum](#rentalperiodtypeenum)
    * [RentalStatusEnum](#rentalstatusenum)
    * [TncAppStage](#tncappstage)
    * [UserStatusEnum](#userstatusenum)
    * [UserTypeEnum](#usertypeenum)
  * [Scalars](#scalars)
    * [Boolean](#boolean)
    * [DateTime](#datetime)
    * [Float](#float)
    * [ID](#id)
    * [Int](#int)
    * [Json](#json)
    * [String](#string)
    * [Upload](#upload)
  * [Interfaces](#interfaces)
    * [MutationResponse](#mutationresponse)
    * [Node](#node)

</details>

## Query 
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>viewer</strong></td>
<td valign="top"><a href="#viewer">Viewer</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>CURRENT_TOS_VERSION</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#rentalwhereuniqueinput">RentalWhereUniqueInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carwhereuniqueinput">CarWhereUniqueInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getCoupon</strong></td>
<td valign="top"><a href="#coupon">Coupon</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">code</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>validateVin</strong></td>
<td valign="top"><a href="#validatevin">ValidateVin</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">vin</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>geoStates</strong></td>
<td valign="top">[<a href="#geostate">GeoState</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getCarPriceBreakdown</strong></td>
<td valign="top"><a href="#carpricebreakdown">CarPriceBreakdown</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">carId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">rentalDays</td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">couponCode</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>offersConnection</strong></td>
<td valign="top"><a href="#carconnection">CarConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#carwhereinput">CarWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#carorderbyinput">CarOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">sortBy</td>
<td valign="top"><a href="#offerssortbyenum">OffersSortByEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>offers</strong></td>
<td valign="top">[<a href="#car">Car</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#carwhereinput">CarWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#carorderbyinput">CarOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>offer</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">offerId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getProspectiveRentalContractUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#prospectiverentalcontractinput">ProspectiveRentalContractInput</a></td>
<td></td>
</tr>
</tbody>
</table>

## Mutation 
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>loginUserWithAuth0Lock</strong></td>
<td valign="top"><a href="#loginuserpayload">LoginUserPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">token</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">type</td>
<td valign="top"><a href="#usertypeenum">UserTypeEnum</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>switchAccount</strong></td>
<td valign="top"><a href="#loginuserpayload">LoginUserPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>acceptCurrentTos</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">tosVersion</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requestBooking</strong></td>
<td valign="top"><a href="#requestbookingpayload">RequestBookingPayload</a></td>
<td>

Car must be available, creates a rental with status APPLIED_NOT_VERIFIED if driver is not verified, or just APPLIED if they are ready to go

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#requestbookinginput">RequestBookingInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateProfilePhoto</strong></td>
<td valign="top"><a href="#updateprofilephotopayload">UpdateProfilePhotoPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#updateprofilephotoinput">UpdateProfilePhotoInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateProfile</strong></td>
<td valign="top"><a href="#updateprofilepayload">UpdateProfilePayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateprofileinput">UpdateProfileInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>uploadDriversLicense</strong></td>
<td valign="top"><a href="#updateprofilepayload">UpdateProfilePayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">photo</td>
<td valign="top"><a href="#upload">Upload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatePaymentInfo</strong></td>
<td valign="top"><a href="#updatepaymentinfopayload">UpdatePaymentInfoPayload</a></td>
<td>

Checks if user already has payment info, and if so, assigns the source. Otherwise, creates new paymentInfo

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#updatepaymentinfoinput">UpdatePaymentInfoInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatePayoutInfo</strong></td>
<td valign="top"><a href="#updatepayoutinfopayload">UpdatePayoutInfoPayload</a></td>
<td>

Checks if user already has payout info, and if so, assigns the source. Otherwise, creates new payoutInfo

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#updatepayoutinfoinput">UpdatePayoutInfoInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startBackgroundCheck</strong></td>
<td valign="top"><a href="#startbackgroundcheckpayload">StartBackgroundCheckPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#startbackgroundcheckinput">StartBackgroundCheckInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>approveBooking</strong></td>
<td valign="top"><a href="#approverejectbookingpayload">ApproveRejectBookingPayload</a></td>
<td>

Rental's car must be owned by current user, specified rental must be in APPLIED status approves specified rental and auto-rejects other rentals that are in APPLIED/APPLIED_NOT_VERIFIED statuses

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#approverejectbookinginput">ApproveRejectBookingInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rejectBooking</strong></td>
<td valign="top"><a href="#approverejectbookingpayload">ApproveRejectBookingPayload</a></td>
<td>

Rental's car must be owned by current user, specified rental must be in APPLIED status

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#approverejectbookinginput">ApproveRejectBookingInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>toggleRentalExtension</strong></td>
<td valign="top"><a href="#togglerentalextensionpayload">ToggleRentalExtensionPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#togglerentalextensioninput">ToggleRentalExtensionInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>confirmDropoff</strong></td>
<td valign="top"><a href="#confirmdropoffpayload">ConfirmDropoffPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#confirmdropoffinput">ConfirmDropoffInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>confirmPickup</strong></td>
<td valign="top"><a href="#confirmpickuppayload">ConfirmPickupPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#confirmpickupinput">ConfirmPickupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rateDriver</strong></td>
<td valign="top"><a href="#ratedriverpayload">RateDriverPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#ratedriverinput">RateDriverInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>toggleListing</strong></td>
<td valign="top"><a href="#togglelistingpayload">ToggleListingPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#togglelistinginput">ToggleListingInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>listCar</strong></td>
<td valign="top"><a href="#listcarpayload">ListCarPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#listcarinput">ListCarInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>removeCarPhoto</strong></td>
<td valign="top"><a href="#addremovecarphotopayload">AddRemoveCarPhotoPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#removecarphotoinput">RemoveCarPhotoInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>addCarPhoto</strong></td>
<td valign="top"><a href="#addremovecarphotopayload">AddRemoveCarPhotoPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#addcarphotoinput">AddCarPhotoInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>uploadCarDocument</strong></td>
<td valign="top"><a href="#uploadcardocumentpayload">UploadCarDocumentPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#uploadcardocumentinput">UploadCarDocumentInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateCarDetails</strong></td>
<td valign="top"><a href="#updatecarpayload">UpdateCarPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#updatecardetailsinput">UpdateCarDetailsInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicateCar</strong></td>
<td valign="top"><a href="#updatecarpayload">UpdateCarPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#duplicatecarinput">DuplicateCarInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>extendRental</strong></td>
<td valign="top"><a href="#extendrentalpayload">ExtendRentalPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#extendrentalinput">ExtendRentalInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createClaimEvidence</strong></td>
<td valign="top"><a href="#createclaimevidencepayload">CreateClaimEvidencePayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#createclaimevidenceinput">CreateClaimEvidenceInput</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Objects

### Accident

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>factOfLoss</strong></td>
<td valign="top"><a href="#factofloss">FactOfLoss</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#factoflosswhereinput">FactOfLossWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top">[<a href="#adminnote">AdminNote</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claim</strong></td>
<td valign="top"><a href="#claim">Claim</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>approvedAmount</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deductible</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimAmount</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>damageLocation</strong></td>
<td valign="top">[<a href="#damagelocation">DamageLocation</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>location</strong></td>
<td valign="top"><a href="#location">Location</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#locationwhereinput">LocationWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tncClaim</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tncUsageDetails</strong></td>
<td valign="top"><a href="#tncusagedetails">TncUsageDetails</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#tncusagedetailswhereinput">TncUsageDetailsWhereInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### AddRemoveCarPhotoPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carPhoto</strong></td>
<td valign="top"><a href="#carphoto">CarPhoto</a></td>
<td></td>
</tr>
</tbody>
</table>

### Admin

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top">[<a href="#adminnote">AdminNote</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>permissions</strong></td>
<td valign="top">[<a href="#adminpermissions">AdminPermissions</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submittedClaims</strong></td>
<td valign="top">[<a href="#claim">Claim</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#claimorderbyinput">ClaimOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>assignedClaims</strong></td>
<td valign="top">[<a href="#claim">Claim</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#claimorderbyinput">ClaimOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
</tbody>
</table>

### AdminNote

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>note</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dueDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>admin</strong></td>
<td valign="top"><a href="#admin">Admin</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminwhereinput">AdminWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driverId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ownerId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>backgroundCheckId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insuranceId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>factOfLoss</strong></td>
<td valign="top"><a href="#factofloss">FactOfLoss</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#factoflosswhereinput">FactOfLossWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>involvedParty</strong></td>
<td valign="top"><a href="#involvedparty">InvolvedParty</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#involvedpartywhereinput">InvolvedPartyWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>evidence</strong></td>
<td valign="top"><a href="#evidence">Evidence</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#evidencewhereinput">EvidenceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accident</strong></td>
<td valign="top"><a href="#accident">Accident</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#accidentwhereinput">AccidentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claim</strong></td>
<td valign="top"><a href="#claim">Claim</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>incidental</strong></td>
<td valign="top"><a href="#incidental">Incidental</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#incidentalwhereinput">IncidentalWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimStatementId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimInvoiceId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>metaDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>meta</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>owner</strong></td>
<td valign="top"><a href="#owner">Owner</a></td>
<td></td>
</tr>
</tbody>
</table>

### AdminNoteConnection

A connection to a list of items.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>pageInfo</strong></td>
<td valign="top"><a href="#pageinfo">PageInfo</a>!</td>
<td>

Information to aid in pagination.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>edges</strong></td>
<td valign="top">[<a href="#adminnoteedge">AdminNoteEdge</a>]!</td>
<td>

A list of edges.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>aggregate</strong></td>
<td valign="top"><a href="#aggregateadminnote">AggregateAdminNote</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AdminNoteEdge

An edge in a connection.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>node</strong></td>
<td valign="top"><a href="#adminnote">AdminNote</a>!</td>
<td>

The item at the end of the edge.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

A cursor for use in pagination.

</td>
</tr>
</tbody>
</table>

### AggregateAdminNote

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>count</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AggregateCar

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>count</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AggregateClaim

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>count</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AggregateInsurance

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>count</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AggregateRating

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>count</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AggregateRental

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>count</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ApproveRejectBookingPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
</tbody>
</table>

### Auth0Details

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nickname</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>picture</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email_verified</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>given_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>family_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user_metadata</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>app_metadata</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>username</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone_number</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone_verified</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>created_at</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updated_at</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>identities</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>multifactor</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>last_ip</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>last_login</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>logins_count</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>blocked</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### BackgroundCheck

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>driver</strong></td>
<td valign="top"><a href="#driver">Driver</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>verificationStatus</strong></td>
<td valign="top"><a href="#driververificationstatusenum">DriverVerificationStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>verifiedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>checkrCandidateId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>licensePhoto</strong> ⚠️</td>
<td valign="top"><a href="#string">String</a></td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

No longer supported

</blockquote>
</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>missingInfo</strong></td>
<td valign="top"><a href="#backgroundcheckmissinginfo">BackgroundCheckMissingInfo</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>checkrStatus</strong></td>
<td valign="top"><a href="#checkrstatusenum">CheckrStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top"><a href="#adminnoteconnection">AdminNoteConnection</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### BackgroundCheckMissingInfo

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>backgroundCheck</strong></td>
<td valign="top"><a href="#backgroundcheck">BackgroundCheck</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#backgroundcheckwhereinput">BackgroundCheckWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>profilePicture</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driverLicense</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>olderDriverLicense</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>address</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>criminalReport</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mvr</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### BackgroundCheckPayment

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>chargeId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>coupon</strong></td>
<td valign="top"><a href="#coupon">Coupon</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#couponwhereinput">CouponWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentAccount</strong></td>
<td valign="top"><a href="#paymentaccount">PaymentAccount</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#paymentaccountwhereinput">PaymentAccountWhereInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### Car

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>completedInspection</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dailyPriceInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>makeId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>make</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modelId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>model</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>yearId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>year</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>instantApprove</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>licensePlate</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mileage</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxDailyMiles</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxWeeklyMiles</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxMonthlyMiles</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>monthlyPriceInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>registrationExpirationAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>vin</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>weeklyPriceInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#marketstatusenum">MarketStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>verification</strong></td>
<td valign="top"><a href="#carstatusenum">CarStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>location</strong></td>
<td valign="top"><a href="#carlocation">CarLocation</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carlocationwhereinput">CarLocationWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tlcCertified</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>photos</strong></td>
<td valign="top">[<a href="#carphoto">CarPhoto</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carphotowhereinput">CarPhotoWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#carphotoorderbyinput">CarPhotoOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>documents</strong></td>
<td valign="top">[<a href="#cardocument">CarDocument</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#cardocumentwhereinput">CarDocumentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#cardocumentorderbyinput">CarDocumentOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>missingInfo</strong></td>
<td valign="top"><a href="#carmissinginfo">CarMissingInfo</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carmissinginfowhereinput">CarMissingInfoWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claims</strong></td>
<td valign="top">[<a href="#claim">Claim</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#claimorderbyinput">ClaimOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top"><a href="#adminnoteconnection">AdminNoteConnection</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>owner</strong></td>
<td valign="top"><a href="#owner">Owner</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentals</strong></td>
<td valign="top"><a href="#rentalconnection">RentalConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#rentalwhereinput">RentalWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentalorderbyinput">RentalOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ratings</strong></td>
<td valign="top"><a href="#ratingconnection">RatingConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#ratingwhereinput">RatingWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#ratingorderbyinput">RatingOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carRatingsMeta</strong></td>
<td valign="top"><a href="#carratingsmeta">CarRatingsMeta</a></td>
<td></td>
</tr>
</tbody>
</table>

### CarConnection

A connection to a list of items.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>pageInfo</strong></td>
<td valign="top"><a href="#pageinfo">PageInfo</a>!</td>
<td>

Information to aid in pagination.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>edges</strong></td>
<td valign="top">[<a href="#caredge">CarEdge</a>]!</td>
<td>

A list of edges.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>aggregate</strong></td>
<td valign="top"><a href="#aggregatecar">AggregateCar</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CarDocument

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#cardocumenttypeenum">CarDocumentTypeEnum</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carwhereinput">CarWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>file</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
</tbody>
</table>

### CarEdge

An edge in a connection.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>node</strong></td>
<td valign="top"><a href="#car">Car</a>!</td>
<td>

The item at the end of the edge.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

A cursor for use in pagination.

</td>
</tr>
</tbody>
</table>

### CarLocation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lat</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lng</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formattedAddress</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>street</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carwhereinput">CarWhereInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### CarMissingInfo

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carwhereinput">CarWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>missingRegistration</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>missingInspection</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>missingPersonalInsurance</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>invalidRegistration</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>invalidInspection</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### CarPhoto

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrimary</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carwhereinput">CarWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>file</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
</tbody>
</table>

### CarPriceBreakdown

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>basePriceBeforeDiscounts</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>weeklyDiscount</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>weeklyDiscountPercent</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>monthlyDiscount</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>monthlyDiscountPercent</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>basePriceAfterLongRentalDiscounts</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>transactionFee</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insuranceFee</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>couponDiscount</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>grandTotal</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>refundableDeposit</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>INSURANCE_CENTS_PER_DAY</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>CENTS_PER_DOLLAR</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>TRANSACTION_FEE</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>REFUNDABLE_DEPOSIT_CENTS</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>numMonths</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>numWeeks</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>numDays</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>coupon</strong></td>
<td valign="top"><a href="#coupon">Coupon</a></td>
<td></td>
</tr>
</tbody>
</table>

### CarRatingsMeta

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>totalRatings</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>avgRating</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
</tbody>
</table>

### Claim

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accident</strong></td>
<td valign="top"><a href="#accident">Accident</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#accidentwhereinput">AccidentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insuranceId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driverId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ownerId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>incidentals</strong></td>
<td valign="top">[<a href="#incidental">Incidental</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#incidentalwhereinput">IncidentalWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#incidentalorderbyinput">IncidentalOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zendeskTicketId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top">[<a href="#adminnote">AdminNote</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>evidences</strong></td>
<td valign="top">[<a href="#evidence">Evidence</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#evidencewhereinput">EvidenceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#evidenceorderbyinput">EvidenceOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#claimstatus">ClaimStatus</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statementId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>assignedAdmin</strong></td>
<td valign="top"><a href="#admin">Admin</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminwhereinput">AdminWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submittedByAdmin</strong></td>
<td valign="top"><a href="#admin">Admin</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminwhereinput">AdminWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submittedByType</strong></td>
<td valign="top"><a href="#claimreportedby">ClaimReportedBy</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>surveyComment</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>meta</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statement</strong></td>
<td valign="top"><a href="#claimstatement">ClaimStatement</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driver</strong></td>
<td valign="top"><a href="#driver">Driver</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>owner</strong></td>
<td valign="top"><a href="#owner">Owner</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fnolPdfUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insurance</strong></td>
<td valign="top"><a href="#insurance">Insurance</a></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimConnection

A connection to a list of items.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>pageInfo</strong></td>
<td valign="top"><a href="#pageinfo">PageInfo</a>!</td>
<td>

Information to aid in pagination.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>edges</strong></td>
<td valign="top">[<a href="#claimedge">ClaimEdge</a>]!</td>
<td>

A list of edges.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>aggregate</strong></td>
<td valign="top"><a href="#aggregateclaim">AggregateClaim</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ClaimEdge

An edge in a connection.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>node</strong></td>
<td valign="top"><a href="#claim">Claim</a>!</td>
<td>

The item at the end of the edge.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

A cursor for use in pagination.

</td>
</tr>
</tbody>
</table>

### ClaimInvoice

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#claiminvoicestatus">ClaimInvoiceStatus</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submittedByAdmin</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statement</strong></td>
<td valign="top"><a href="#claimstatement">ClaimStatement</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimstatementwhereinput">ClaimStatementWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>oldStatement</strong></td>
<td valign="top"><a href="#claimstatement">ClaimStatement</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimstatementwhereinput">ClaimStatementWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>adminFeeInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>referenceId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>meta</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>overview</strong></td>
<td valign="top"><a href="#claiminvoiceoverview">ClaimInvoiceOverview</a></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimInvoiceItem

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>amountInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimInvoiceOverview

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>bookingDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pickupDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dropOffDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ownerName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>items</strong></td>
<td valign="top">[<a href="#claiminvoiceitem">ClaimInvoiceItem</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimPayment

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>chargeId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentAccount</strong></td>
<td valign="top"><a href="#paymentaccount">PaymentAccount</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#paymentaccountwhereinput">PaymentAccountWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>amountInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimStatement</strong></td>
<td valign="top"><a href="#claimstatement">ClaimStatement</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimstatementwhereinput">ClaimStatementWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paidBy</strong></td>
<td valign="top"><a href="#claimpaidbyparty">ClaimPaidByParty</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>meta</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimStatement

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#claimpaymentplanstatus">ClaimPaymentPlanStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>managedBy</strong></td>
<td valign="top"><a href="#claimpaymentplanmanager">ClaimPaymentPlanManager</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submittedByAdmin</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submittedByUserId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>assigedAdmin</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>numberOfPayments</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paidInFullBy</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>planPeriod</strong></td>
<td valign="top"><a href="#claimpaymentplanperiod">ClaimPaymentPlanPeriod</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driverId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>invoice</strong></td>
<td valign="top"><a href="#claiminvoice">ClaimInvoice</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claiminvoicewhereinput">ClaimInvoiceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>invoices</strong></td>
<td valign="top">[<a href="#claiminvoice">ClaimInvoice</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claiminvoicewhereinput">ClaimInvoiceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#claiminvoiceorderbyinput">ClaimInvoiceOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deposit</strong></td>
<td valign="top"><a href="#deposit">Deposit</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#depositwhereinput">DepositWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>payments</strong></td>
<td valign="top">[<a href="#claimpayment">ClaimPayment</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimpaymentwhereinput">ClaimPaymentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#claimpaymentorderbyinput">ClaimPaymentOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submittedByUser</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submittedBy</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConfirmDropoffPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConfirmPickupPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
</tbody>
</table>

### Coupon

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>legacyId</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>discountInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isBgc</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDeposit</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDollar</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isLateFee</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>limit</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>backgroundCheckPayments</strong></td>
<td valign="top">[<a href="#backgroundcheckpayment">BackgroundCheckPayment</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#backgroundcheckpaymentwhereinput">BackgroundCheckPaymentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#backgroundcheckpaymentorderbyinput">BackgroundCheckPaymentOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deposits</strong></td>
<td valign="top">[<a href="#deposit">Deposit</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#depositwhereinput">DepositWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#depositorderbyinput">DepositOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalPayments</strong></td>
<td valign="top">[<a href="#rentalpayment">RentalPayment</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#rentalpaymentwhereinput">RentalPaymentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentalpaymentorderbyinput">RentalPaymentOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalLateFees</strong></td>
<td valign="top">[<a href="#rentallatefeepayment">RentalLateFeePayment</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#rentallatefeepaymentwhereinput">RentalLateFeePaymentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentallatefeepaymentorderbyinput">RentalLateFeePaymentOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateClaimEvidencePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>evidence</strong></td>
<td valign="top"><a href="#evidence">Evidence</a></td>
<td></td>
</tr>
</tbody>
</table>

### Deposit

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>amountWithheldInCents</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>chargeId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isHeld</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isRefunded</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>charge</strong></td>
<td valign="top"><a href="#stripecharge">StripeCharge</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentAccount</strong></td>
<td valign="top"><a href="#paymentaccount">PaymentAccount</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>coupon</strong></td>
<td valign="top"><a href="#coupon">Coupon</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statement</strong></td>
<td valign="top"><a href="#claimstatement">ClaimStatement</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
</tbody>
</table>

### Driver

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>aboutMe</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legacyId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>blockedFromBooking</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legalInfo</strong></td>
<td valign="top"><a href="#driverlegalinfo">DriverLegalInfo</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>backgroundCheck</strong></td>
<td valign="top"><a href="#backgroundcheck">BackgroundCheck</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>licensePhotoId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requiresTncAcceptance</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claims</strong></td>
<td valign="top">[<a href="#claim">Claim</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#claimorderbyinput">ClaimOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimsConnection</strong></td>
<td valign="top"><a href="#claimconnection">ClaimConnection</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#claimorderbyinput">ClaimOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driverClaimsMeta</strong></td>
<td valign="top"><a href="#driverclaimsmeta">DriverClaimsMeta</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top"><a href="#adminnoteconnection">AdminNoteConnection</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentals</strong></td>
<td valign="top"><a href="#rentalconnection">RentalConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#rentalwhereinput">RentalWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentalorderbyinput">RentalOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>licensePhoto</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ratings</strong></td>
<td valign="top"><a href="#ratingconnection">RatingConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#ratingwhereinput">RatingWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#ratingorderbyinput">RatingOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driverRatingsMeta</strong></td>
<td valign="top"><a href="#driverratingsmeta">DriverRatingsMeta</a></td>
<td></td>
</tr>
</tbody>
</table>

### DriverClaimsMeta

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>rentalWithClaimsCount</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalAccidents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalIncidents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalClaims</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### DriverLegalInfo

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>driver</strong></td>
<td valign="top"><a href="#driver">Driver</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dob</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>licensePhotoId</strong> ⚠️</td>
<td valign="top"><a href="#id">ID</a></td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

No longer supported

</blockquote>
</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legalFirstName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legalLastName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legalMiddleName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>licenseNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>licenseState</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>licenseExpirationDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fullName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>licensePhoto</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
</tbody>
</table>

### DriverRatingsMeta

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>totalRatings</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>avgRating</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
</tbody>
</table>

### Evidence

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top">[<a href="#adminnote">AdminNote</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claim</strong></td>
<td valign="top"><a href="#claim">Claim</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileType</strong></td>
<td valign="top"><a href="#evidencefiletype">EvidenceFileType</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#evidencetype">EvidenceType</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>file</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
</tbody>
</table>

### ExtendRentalPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalPeriod</strong></td>
<td valign="top"><a href="#rentalperiod">RentalPeriod</a></td>
<td></td>
</tr>
</tbody>
</table>

### FactOfLoss

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accident</strong></td>
<td valign="top"><a href="#accident">Accident</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#accidentwhereinput">AccidentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>damageType</strong></td>
<td valign="top"><a href="#damagetype">DamageType</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dateOfIncident</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top">[<a href="#adminnote">AdminNote</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>involvedParty</strong></td>
<td valign="top"><a href="#involvedparty">InvolvedParty</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#involvedpartywhereinput">InvolvedPartyWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>policeReport</strong></td>
<td valign="top"><a href="#policereport">PoliceReport</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#policereportwhereinput">PoliceReportWhereInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### File

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>size</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>secret</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contentType</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#filetypeenum">FileTypeEnum</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>path</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thumbnailPath</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#fileurlwhereinput">FileUrlWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thumbnailUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### GeoState

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Incidental

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>comment</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claim</strong></td>
<td valign="top"><a href="#claim">Claim</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top">[<a href="#adminnote">AdminNote</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimAmount</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>approvedAmount</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#incidentaltype">IncidentalType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>meta</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
</tbody>
</table>

### Insurance

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contractId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>vin</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>applicationId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insuranceCardImageId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#insurancestatus">InsuranceStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startDateTime</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>endDateTime</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pre</strong></td>
<td valign="top"><a href="#preinsurance">PreInsurance</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#preinsurancewhereinput">PreInsuranceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>post</strong></td>
<td valign="top"><a href="#postinsurance">PostInsurance</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#postinsurancewhereinput">PostInsuranceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insuranceCardImage</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claim</strong></td>
<td valign="top"><a href="#claim">Claim</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top"><a href="#adminnoteconnection">AdminNoteConnection</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### InsuranceConnection

A connection to a list of items.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>pageInfo</strong></td>
<td valign="top"><a href="#pageinfo">PageInfo</a>!</td>
<td>

Information to aid in pagination.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>edges</strong></td>
<td valign="top">[<a href="#insuranceedge">InsuranceEdge</a>]!</td>
<td>

A list of edges.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>aggregate</strong></td>
<td valign="top"><a href="#aggregateinsurance">AggregateInsurance</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### InsuranceEdge

An edge in a connection.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>node</strong></td>
<td valign="top"><a href="#insurance">Insurance</a>!</td>
<td>

The item at the end of the edge.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

A cursor for use in pagination.

</td>
</tr>
</tbody>
</table>

### InvolvedParty

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top">[<a href="#adminnote">AdminNote</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>factOfLoss</strong></td>
<td valign="top"><a href="#factofloss">FactOfLoss</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#factoflosswhereinput">FactOfLossWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insuranceCarrier</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>policyNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#involvedpartytype">InvolvedPartyType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>comment</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>adjustorInfo</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phoneNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ListCarPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
</tbody>
</table>

### Location

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accident</strong></td>
<td valign="top"><a href="#accident">Accident</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#accidentwhereinput">AccidentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lat</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lng</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>street</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### LoginUserPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>token</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isNewUser</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### Owner

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>aboutMe</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legacyId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>verified</strong> ⚠️</td>
<td valign="top"><a href="#int">Int</a></td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

No longer supported

</blockquote>
</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claims</strong></td>
<td valign="top">[<a href="#claim">Claim</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#claimwhereinput">ClaimWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#claimorderbyinput">ClaimOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top"><a href="#adminnoteconnection">AdminNoteConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cars</strong></td>
<td valign="top"><a href="#carconnection">CarConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carwhereinput">CarWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#carorderbyinput">CarOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalsConnection</strong></td>
<td valign="top"><a href="#rentalconnection">RentalConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#rentalwhereinput">RentalWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentalorderbyinput">RentalOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentals</strong></td>
<td valign="top">[<a href="#rental">Rental</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#rentalwhereinput">RentalWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentalorderbyinput">RentalOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### PageInfo

Information about pagination in a connection.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>hasNextPage</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td>

When paginating forwards, are there more items?

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hasPreviousPage</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td>

When paginating backwards, are there more items?

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startCursor</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

When paginating backwards, the cursor to continue.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>endCursor</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

When paginating forwards, the cursor to continue.

</td>
</tr>
</tbody>
</table>

### PaymentAccount

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#paymentprovidertypeenum">PaymentProviderTypeEnum</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#paymentaccountstatusenum">PaymentAccountStatusEnum</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legacyUserId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deposits</strong></td>
<td valign="top">[<a href="#deposit">Deposit</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#depositwhereinput">DepositWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#depositorderbyinput">DepositOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>stripePaymentInformation</strong></td>
<td valign="top"><a href="#stripepaymentinformation">StripePaymentInformation</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#stripepaymentinformationwhereinput">StripePaymentInformationWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalPayments</strong></td>
<td valign="top">[<a href="#rentalpayment">RentalPayment</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#rentalpaymentwhereinput">RentalPaymentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentalpaymentorderbyinput">RentalPaymentOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>backgroundCheckPayment</strong></td>
<td valign="top"><a href="#backgroundcheckpayment">BackgroundCheckPayment</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#backgroundcheckpaymentwhereinput">BackgroundCheckPaymentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalLateFeePayments</strong></td>
<td valign="top">[<a href="#rentallatefeepayment">RentalLateFeePayment</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#rentallatefeepaymentwhereinput">RentalLateFeePaymentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentallatefeepaymentorderbyinput">RentalLateFeePaymentOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claimPayments</strong></td>
<td valign="top">[<a href="#claimpayment">ClaimPayment</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#claimpaymentwhereinput">ClaimPaymentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#claimpaymentorderbyinput">ClaimPaymentOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### PayoutAccount

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#paymentprovidertypeenum">PaymentProviderTypeEnum</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legacyUserId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>stripePayoutInformation</strong></td>
<td valign="top"><a href="#stripepayoutinformation">StripePayoutInformation</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#stripepayoutinformationwhereinput">StripePayoutInformationWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### PoliceReport

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>policeDepartment</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reportNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>factOfLoss</strong></td>
<td valign="top"><a href="#factofloss">FactOfLoss</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#factoflosswhereinput">FactOfLossWhereInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### PostInsurance

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insurance</strong></td>
<td valign="top"><a href="#insurance">Insurance</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#insurancewhereinput">InsuranceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDamaged</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isGasLower</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isLate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isMileageExceeded</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### PreInsurance

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pickedUpAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requestedPickupAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insurance</strong></td>
<td valign="top"><a href="#insurance">Insurance</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#insurancewhereinput">InsuranceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDriverIdentified</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>photos</strong></td>
<td valign="top">[<a href="#preinsurancephoto">PreInsurancePhoto</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#preinsurancephotowhereinput">PreInsurancePhotoWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#preinsurancephotoorderbyinput">PreInsurancePhotoOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### PreInsurancePhoto

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#preinsurancephototypeenum">PreInsurancePhotoTypeEnum</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>preInsurance</strong></td>
<td valign="top"><a href="#preinsurance">PreInsurance</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#preinsurancewhereinput">PreInsuranceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>file</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
</tbody>
</table>

### RateDriverPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rating</strong></td>
<td valign="top"><a href="#rating">Rating</a></td>
<td></td>
</tr>
</tbody>
</table>

### Rating

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>comment</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>revieweeId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reviewerId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rating</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>helpful</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#ratingtype">RatingType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
</tbody>
</table>

### RatingConnection

A connection to a list of items.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>pageInfo</strong></td>
<td valign="top"><a href="#pageinfo">PageInfo</a>!</td>
<td>

Information to aid in pagination.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>edges</strong></td>
<td valign="top">[<a href="#ratingedge">RatingEdge</a>]!</td>
<td>

A list of edges.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>aggregate</strong></td>
<td valign="top"><a href="#aggregaterating">AggregateRating</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RatingEdge

An edge in a connection.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>node</strong></td>
<td valign="top"><a href="#rating">Rating</a>!</td>
<td>

The item at the end of the edge.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

A cursor for use in pagination.

</td>
</tr>
</tbody>
</table>

### Rental

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legacyApplicationId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legacyRentalId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>disallowExtensions</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#rentalstatusenum">RentalStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cancellationReason</strong></td>
<td valign="top"><a href="#rentalcancellationtypeenum">RentalCancellationTypeEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalPeriods</strong></td>
<td valign="top">[<a href="#rentalperiod">RentalPeriod</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#rentalperiodwhereinput">RentalPeriodWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentalperiodorderbyinput">RentalPeriodOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currentRentalPeriod</strong></td>
<td valign="top"><a href="#rentalperiod">RentalPeriod</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driverId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>depositId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requestedPickupAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>droppedOffAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ownerApprovedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top"><a href="#adminnoteconnection">AdminNoteConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driver</strong></td>
<td valign="top"><a href="#driver">Driver</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>driverRating</strong></td>
<td valign="top"><a href="#rating">Rating</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carRating</strong></td>
<td valign="top"><a href="#rating">Rating</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>claim</strong></td>
<td valign="top"><a href="#claim">Claim</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deposit</strong></td>
<td valign="top"><a href="#deposit">Deposit</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insurance</strong></td>
<td valign="top"><a href="#insurance">Insurance</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insurances</strong></td>
<td valign="top">[<a href="#insurance">Insurance</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#insurancewhereinput">InsuranceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#insuranceorderbyinput">InsuranceOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insurancesConnection</strong></td>
<td valign="top"><a href="#insuranceconnection">InsuranceConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#insurancewhereinput">InsuranceWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#insuranceorderbyinput">InsuranceOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>overview</strong></td>
<td valign="top"><a href="#rentaloverview">RentalOverview</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>prospectiveRentalContractUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### RentalConnection

A connection to a list of items.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>pageInfo</strong></td>
<td valign="top"><a href="#pageinfo">PageInfo</a>!</td>
<td>

Information to aid in pagination.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>edges</strong></td>
<td valign="top">[<a href="#rentaledge">RentalEdge</a>]!</td>
<td>

A list of edges.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>aggregate</strong></td>
<td valign="top"><a href="#aggregaterental">AggregateRental</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RentalEdge

An edge in a connection.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>node</strong></td>
<td valign="top"><a href="#rental">Rental</a>!</td>
<td>

The item at the end of the edge.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

A cursor for use in pagination.

</td>
</tr>
</tbody>
</table>

### RentalLateFeePayment

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>amountInCents</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>coupon</strong></td>
<td valign="top"><a href="#coupon">Coupon</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#couponwhereinput">CouponWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>chargeId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentAccount</strong></td>
<td valign="top"><a href="#paymentaccount">PaymentAccount</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#paymentaccountwhereinput">PaymentAccountWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalPayment</strong></td>
<td valign="top"><a href="#rentalpayment">RentalPayment</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#rentalpaymentwhereinput">RentalPaymentWhereInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### RentalOverview

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalDays</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>endDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>daysRemaining</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hoursRemaining</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ownerEarningsInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalCostInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalPaidInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lateFeeCaptured</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### RentalPayment

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>chargeId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentAccount</strong></td>
<td valign="top"><a href="#paymentaccount">PaymentAccount</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#paymentaccountwhereinput">PaymentAccountWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>basePriceInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>transactionFeeInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insuranceFeeInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>couponDiscountInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>grandTotalInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ownerEarningsInCents</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>coupon</strong></td>
<td valign="top"><a href="#coupon">Coupon</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#couponwhereinput">CouponWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalPeriodId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legacyRentalPeriodId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalLateFeePayment</strong></td>
<td valign="top"><a href="#rentallatefeepayment">RentalLateFeePayment</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#rentallatefeepaymentwhereinput">RentalLateFeePaymentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>capture</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalPeriod</strong></td>
<td valign="top"><a href="#rentalperiod">RentalPeriod</a></td>
<td></td>
</tr>
</tbody>
</table>

### RentalPeriod

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legacyExtensionId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#rentalwhereinput">RentalWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>endDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>numDays</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalContractId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#rentalperiodtypeenum">RentalPeriodTypeEnum</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentalContract</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>payment</strong></td>
<td valign="top"><a href="#rentalpayment">RentalPayment</a></td>
<td></td>
</tr>
</tbody>
</table>

### RequestBookingPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
</tbody>
</table>

### StartBackgroundCheckPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>backgroundCheck</strong></td>
<td valign="top"><a href="#backgroundcheck">BackgroundCheck</a></td>
<td></td>
</tr>
</tbody>
</table>

### StripeCharge

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>captured</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### StripePaymentInformation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>customerId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentAccount</strong></td>
<td valign="top"><a href="#paymentaccount">PaymentAccount</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>source</strong></td>
<td valign="top"><a href="#stripepaymentsource">StripePaymentSource</a></td>
<td></td>
</tr>
</tbody>
</table>

### StripePaymentSource

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>last4</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>brand</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>funding</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### StripePayoutBank

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>last4</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>bankName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### StripePayoutInformation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentAccount</strong></td>
<td valign="top"><a href="#payoutaccount">PayoutAccount</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>bank</strong></td>
<td valign="top"><a href="#stripepayoutbank">StripePayoutBank</a></td>
<td></td>
</tr>
</tbody>
</table>

### TncUsageDetails

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accident</strong></td>
<td valign="top"><a href="#accident">Accident</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#accidentwhereinput">AccidentWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top">[<a href="#adminnote">AdminNote</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#adminnotewhereinput">AdminNoteWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#adminnoteorderbyinput">AdminNoteOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>passengerIdentifications</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>passengers</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tncAppOnDuringIncident</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tncStage</strong></td>
<td valign="top"><a href="#tncappstage">TncAppStage</a></td>
<td></td>
</tr>
</tbody>
</table>

### ToggleListingPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
</tbody>
</table>

### ToggleRentalExtensionPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rental</strong></td>
<td valign="top"><a href="#rental">Rental</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateCarPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>car</strong></td>
<td valign="top"><a href="#car">Car</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdatePaymentInfoPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentAccount</strong></td>
<td valign="top"><a href="#paymentaccount">PaymentAccount</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdatePayoutInfoPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>payoutAccount</strong></td>
<td valign="top"><a href="#payoutaccount">PayoutAccount</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateProfilePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateProfilePhotoPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>file</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
</tbody>
</table>

### UploadCarDocumentPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>carDocument</strong></td>
<td valign="top"><a href="#cardocument">CarDocument</a></td>
<td></td>
</tr>
</tbody>
</table>

### User

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>driver</strong></td>
<td valign="top"><a href="#driver">Driver</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>firstName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hyrecarTosAcceptedVersion</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hyrecarTosAcceptedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>legacyId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>auth0Id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastLoginAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>location</strong></td>
<td valign="top"><a href="#userlocation">UserLocation</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>owner</strong></td>
<td valign="top"><a href="#owner">Owner</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>profilePhotoId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#userstatusenum">UserStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#usertypeenum">UserTypeEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>roles</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>typeId</strong> ⚠️</td>
<td valign="top"><a href="#int">Int</a></td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

No longer supported

</blockquote>
</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>photo</strong> ⚠️</td>
<td valign="top"><a href="#string">String</a></td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

No longer supported

</blockquote>
</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dob</strong> ⚠️</td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

No longer supported

</blockquote>
</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>auth0Details</strong></td>
<td valign="top"><a href="#auth0details">Auth0Details</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fullName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requiresTosAcceptance</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>admin</strong></td>
<td valign="top"><a href="#admin">Admin</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentAccounts</strong></td>
<td valign="top">[<a href="#paymentaccount">PaymentAccount</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#paymentaccountwhereinput">PaymentAccountWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#paymentaccountorderbyinput">PaymentAccountOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>payoutAccounts</strong></td>
<td valign="top">[<a href="#payoutaccount">PayoutAccount</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#payoutaccountwhereinput">PayoutAccountWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#payoutaccountorderbyinput">PayoutAccountOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>depositOnFile</strong></td>
<td valign="top"><a href="#deposit">Deposit</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>profilePhoto</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
</tbody>
</table>

### UserLocation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formattedAddress</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>street</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lat</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lng</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>apt</strong> ⚠️</td>
<td valign="top"><a href="#string">String</a></td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

No longer supported

</blockquote>
</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>address</strong> ⚠️</td>
<td valign="top"><a href="#string">String</a></td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

No longer supported

</blockquote>
</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>verified</strong> ⚠️</td>
<td valign="top"><a href="#int">Int</a></td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

No longer supported

</blockquote>
</td>
</tr>
</tbody>
</table>

### ValidateVin

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Viewer

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>me</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>admin</strong></td>
<td valign="top"><a href="#admin">Admin</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cars</strong></td>
<td valign="top"><a href="#carconnection">CarConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#carwhereinput">CarWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#carorderbyinput">CarOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentals</strong></td>
<td valign="top"><a href="#rentalconnection">RentalConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#rentalwhereinput">RentalWhereInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">orderBy</td>
<td valign="top"><a href="#rentalorderbyinput">RentalOrderByInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">skip</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">before</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">last</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

## Enums

### AdminNoteOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>note_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>note_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>dueDate_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>dueDate_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>driverId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>driverId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>backgroundCheckId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>backgroundCheckId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>insuranceId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>insuranceId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>claimStatementId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>claimStatementId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>claimInvoiceId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>claimInvoiceId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>metaDate_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>metaDate_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### AdminPermissions

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>CLAIMS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TIER1</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TIER2</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SALES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COLLECTIONS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DRIVER_VERIFICATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LATE_RENTAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DRIVER_SALES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SALES_MANAGER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OWNER_SALES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPS_MANAGER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ADMIN</strong></td>
<td></td>
</tr>
</tbody>
</table>

### BackgroundCheckPaymentOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CarDocumentOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>fileId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>fileId_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CarDocumentTypeEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>REGISTRATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UBER_LYFT_INSPECTION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PERSONAL_INSURANCE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CarOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>completedInspection_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>completedInspection_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>dailyPriceInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>dailyPriceInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>description_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>description_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>makeId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>makeId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>make_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>make_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>modelId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>modelId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>model_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>model_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>yearId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>yearId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>year_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>year_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>instantApprove_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>instantApprove_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>licensePlate_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>licensePlate_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>mileage_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>mileage_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>maxDailyMiles_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>maxDailyMiles_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>maxWeeklyMiles_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>maxWeeklyMiles_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>maxMonthlyMiles_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>maxMonthlyMiles_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>monthlyPriceInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>monthlyPriceInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>registrationExpirationAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>registrationExpirationAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>vin_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>vin_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>weeklyPriceInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>weeklyPriceInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>verification_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>verification_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>tlcCertified_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>tlcCertified_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CarPhotoOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>fileId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>fileId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>isPrimary_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>isPrimary_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CarStatusEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>VERIFIED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PENDING_VERIFICATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FAILED_VERIFICATION</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CheckrStatusEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>PENDING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CLEAR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CONSIDER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DISPUTE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SUSPENDED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimInvoiceOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>submittedByAdmin_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>submittedByAdmin_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>adminFeeInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>adminFeeInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>referenceId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>referenceId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>claimId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>claimId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimInvoiceStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>CLOSED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPEN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PAID</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CANCELED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>insuranceId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>insuranceId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>driverId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>driverId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>zendeskTicketId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>zendeskTicketId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>statementId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>statementId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>submittedByType_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>submittedByType_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>surveyComment_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>surveyComment_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimPaidByParty

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>TNC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>THIRD_PARTY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DRIVER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HYRECAR</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimPaymentOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>amountInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>amountInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>paidBy_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>paidBy_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimPaymentPlanManager

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>HC_MANAGED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HC_PAYMENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OFF_PLATFORM</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimPaymentPlanPeriod

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>MONTHLY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>WEEKLY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>BIWEEKLY</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimPaymentPlanStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>OPEN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PAID_IN_FULL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COLLECTIONS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SETTLED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_STARTED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimReportedBy

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>OWNER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ADMIN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DRIVER</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ClaimStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>REPORTED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FALSE_CLAIM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>GATHERING_INFO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CREDIBILITY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FIGHTBACK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PAYMENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SETTLED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SENT_TO_UNDERWRITER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SELF_SETTLEMENT_NEGOTIATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SENT_TO_FAIR_CLAIMS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SENT_TO_YORK_CLAIMS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DENIED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SENT_TO_TNC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>THIRD_PARTY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COLLECTIONS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DELETED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### DamageLocation

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>FRONT_BUMPER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_ROCKER_PANEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_FRONT_BUMPER_CORNER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_ROCKER_PANEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HOOD</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_REAR_DOOR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_FRONT_BUMPER_CORNER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_REAR_DOOR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_FRONT_WHEEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_REAR_WHEEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_FRONT_WHEEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_REAR_WHEEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_FENDER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_QUARTER_PANEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_FENDER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_QUARTER_PANEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_FRONT_DOOR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_REAR_CORNER_BUMPER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_FRONT_DOOR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_REAR_CORNER_BUMPER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_MIRROR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TRUNK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_MIRROR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>REAR_BUMPER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_ROOF_RAIL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPOILER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_ROOF_RAIL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>WHEEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ENGINE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_TAIL_LIGHT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_TAIL_LIGHT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIGHT_HEADLIGHT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LEFT_HEADLIGHT</strong></td>
<td></td>
</tr>
</tbody>
</table>

### DamageType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>STOLEN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TOTAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NA</strong></td>
<td></td>
</tr>
</tbody>
</table>

### DepositOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>amountWithheldInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>amountWithheldInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>isHeld_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>isHeld_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>isRefunded_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>isRefunded_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>isUsed_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>isUsed_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### DriverVerificationStatusEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NOTAPPLIED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>APPLIED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VERIFIED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>REJECTED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNRESPONSIVE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### EvidenceFileType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DOCUMENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IMAGE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### EvidenceOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>fileId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>fileId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>fileType_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>fileType_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### EvidenceType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>INCIDENTAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ACCIDENT</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FileTypeEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>PROFILE_PHOTO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LICENSE_PHOTO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RENTAL_CONTRACT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RENTAL_INSURANCE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_PHOTO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_PICKUP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_DOCUMENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_REGISTRATION_FILE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UBER_LYFT_INSPECTION_FILE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PERSONAL_INSURANCE_FILE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CLAIM_EVIDENCE_FILE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### IncidentalOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>comment_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>comment_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>claimAmount_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>claimAmount_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>approvedAmount_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>approvedAmount_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>meta_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### IncidentalType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>MINOR_DAMAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CLEANING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>GAS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TICKET</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TOLL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MILEAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OTHER</strong></td>
<td></td>
</tr>
</tbody>
</table>

### InsuranceOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>contractId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>contractId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>vin_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>vin_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>applicationId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>applicationId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>insuranceCardImageId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>insuranceCardImageId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>startDateTime_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>startDateTime_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>endDateTime_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>endDateTime_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### InsuranceStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ACTIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CANCELED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CLOSED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### InvolvedPartyType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>WITNESS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CLAIMANT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ADVERSE_PARTY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INSURANCE_AGENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LAWYER</strong></td>
<td></td>
</tr>
</tbody>
</table>

### MarketStatusEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>AVAILABLE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>REMOVED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RENTED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### OffersSortByEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>RELEVANCE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PRICE_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PRICE_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DISTANCE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PaymentAccountOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>userId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>userId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyUserId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyUserId_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PaymentAccountStatusEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>PRIMARY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SECONDARY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INACTIVE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PaymentProviderTypeEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>STRIPE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PayoutAccountOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>userId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>userId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyUserId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyUserId_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PreInsurancePhotoOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>fileId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>fileId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PreInsurancePhotoTypeEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>GENERAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_BACK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_FRONT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_GAS_LEVEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_MILEAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_PASSENGER_SIDE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CAR_DRIVER_SIDE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RatingOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>comment_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>comment_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>revieweeId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>revieweeId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>reviewerId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>reviewerId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rating_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rating_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>helpful_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>helpful_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RatingType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>CAR_RATING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DRIVER_RATING</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RentalCancellationTypeEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>OWNER_CANCELLED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DRIVER_CANCELLED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RentalLateFeePaymentOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>amountInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>amountInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RentalOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyApplicationId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyApplicationId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyRentalId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyRentalId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>disallowExtensions_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>disallowExtensions_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>status_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>cancellationReason_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>cancellationReason_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>driverId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>driverId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>depositId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>depositId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>requestedPickupAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>requestedPickupAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerApprovedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerApprovedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>droppedOffAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>droppedOffAt_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RentalPaymentOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>chargeId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>basePriceInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>basePriceInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>transactionFeeInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>transactionFeeInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>insuranceFeeInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>insuranceFeeInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>couponDiscountInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>couponDiscountInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>grandTotalInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>grandTotalInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerEarningsInCents_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ownerEarningsInCents_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalPeriodId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalPeriodId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyRentalPeriodId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyRentalPeriodId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>capture_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>capture_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RentalPeriodOrderByInput

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>id_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>id_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyExtensionId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>legacyExtensionId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>carId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>createdAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>updatedAt_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>endDate_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>endDate_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>numDays_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>numDays_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>paymentId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>paymentId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalContractId_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>rentalContractId_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>startDate_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>startDate_DESC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>type_DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RentalPeriodTypeEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>INITIAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EXTENSION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VOID</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RentalStatusEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>APPLIED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>APPLIED_NOT_VERIFIED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>APPLICATION_REJECTED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>APPLICATION_EXPIRED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>APPLICATION_AUTO_REJECTED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PENDING_INSURANCE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CANCELLED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PENDING_PICKUP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ACTIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COMPLETED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ARCHIVED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### TncAppStage

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ON</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ASSIGNMENT_RECIEVED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FARE_IN_VEHICLE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OFF</strong></td>
<td></td>
</tr>
</tbody>
</table>

### UserStatusEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ACTIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>BLOCKED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### UserTypeEnum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DRIVER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OWNER</strong></td>
<td></td>
</tr>
</tbody>
</table>

## Scalars

### Boolean

The `Boolean` scalar type represents `true` or `false`.

### DateTime

### Float

The `Float` scalar type represents signed double-precision fractional values as specified by [IEEE 754](http://en.wikipedia.org/wiki/IEEE_floating_point). 

### ID

The `ID` scalar type represents a unique identifier, often used to refetch an object or as key for a cache. The ID type appears in a JSON response as a String; however, it is not intended to be human-readable. When expected as an input type, any string (such as `"4"`) or integer (such as `4`) input value will be accepted as an ID.

### Int

The `Int` scalar type represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1. 

### Json

Raw JSON value

### String

The `String` scalar type represents textual data, represented as UTF-8 character sequences. The String type is most often used by GraphQL to represent free-form human-readable text.

### Upload


## Interfaces


### MutationResponse

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>success</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Node

An object with an ID

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

The id of the object.

</td>
</tr>
</tbody>
</table>
