---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzRegulatoryComplainceAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplainceAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplainceAssessment.md
ms.openlocfilehash: aadafa66c07df178be09bcfefc2e4a2680e3814d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927571"
---
# <span data-ttu-id="c6524-101">Get-AzRegulatoryComplainceAssessment</span><span class="sxs-lookup"><span data-stu-id="c6524-101">Get-AzRegulatoryComplainceAssessment</span></span>

## <span data-ttu-id="c6524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6524-102">SYNOPSIS</span></span>
<span data-ttu-id="c6524-103">Ruft Compliancebewertungen für gesetzliche Vorschriften ab</span><span class="sxs-lookup"><span data-stu-id="c6524-103">Gets regulatory compliance assessments</span></span>

## <span data-ttu-id="c6524-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6524-104">SYNTAX</span></span>

### <span data-ttu-id="c6524-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6524-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplainceAssessment [-Name <String>] -StandardName <String> -ControlName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6524-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6524-106">ResourceId</span></span>
```
Get-AzRegulatoryComplainceAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6524-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6524-107">DESCRIPTION</span></span>
<span data-ttu-id="c6524-108">Erhalten Sie eine spezifische Bewertungsdetails, oder listen Sie alle Bewertungen unter bestimmten Steuerelementen und gesetzlichen Compliancestandards auf.</span><span class="sxs-lookup"><span data-stu-id="c6524-108">Get a spcific assessment details or list all the assessments under specific control and regulatory compliance standard.</span></span>

## <span data-ttu-id="c6524-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6524-109">EXAMPLES</span></span>

### <span data-ttu-id="c6524-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6524-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplainceAssessment -StandardName "SOC TSP" -ControlName "CC5.8"

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/0392
                        b393-395e-42bf-ba60-8d99efc4d2d4
Name                  : 0392b393-395e-42bf-ba60-8d99efc4d2d4
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-10596-5] Deny log on as a batch job (Windows Server 2008 R2 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/04c8
                        24de-a93c-49cf-bb22-997cdff9e9fc
Name                  : 04c824de-a93c-49cf-bb22-997cdff9e9fc
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-24406-1] Allow log on through Remote Desktop Services (Windows Server 2012 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/04e7
                        147b-0deb-9796-2e5c-0336343ceb3d
Name                  : 04e7147b-0deb-9796-2e5c-0336343ceb3d
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : External accounts with write permissions should be removed from your subscription
AssessmentType        : AssessmentResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 1
FailedResources       : 0
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/0515
                        45a4-179e-4c04-9e9b-8f33821ef36f
Name                  : 051545a4-179e-4c04-9e9b-8f33821ef36f
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-37659-0] Configure 'Allow log on locally' (Windows Server 2016 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Failed
PassedResources       : 1
FailedResources       : 1
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/101e
                        af81-3dd3-4867-8871-f649131a06a9
Name                  : 101eaf81-3dd3-4867-8871-f649131a06a9
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-38028-7] Audit Policy: Policy Change: Audit Policy Change (Windows Server 2012 R2
                        Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/103d
                        e8e8-643e-4b0e-b4a4-a85830239a53
Name                  : 103de8e8-643e-4b0e-b4a4-a85830239a53
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-37133-6] Ensure 'Audit Account Lockout' is set to 'Success and Failure' (Windows Server
                        2016 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Failed
PassedResources       : 1
FailedResources       : 1
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/107b
                        8424-7ee8-4b6a-a859-b5256aa6596e
Name                  : 107b8424-7ee8-4b6a-a859-b5256aa6596e
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-37853-9] Audit Policy: System: IPsec Driver (Windows Server 2012 R2 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0
```

<span data-ttu-id="c6524-111">Erhalten Sie alle Bewertungen unter bestimmten Steuerelementen und Standards.</span><span class="sxs-lookup"><span data-stu-id="c6524-111">Get all assessments under specific control and standard.</span></span>

### <span data-ttu-id="c6524-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c6524-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplainceAssessment -StandardName "SOC TSP" -ControlName "CC5.8" -Name "fe48038b-f73a-4264-b499-0ff9dfaab05c"

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/fe48
                        038b-f73a-4264-b499-0ff9dfaab05c
Name                  : fe48038b-f73a-4264-b499-0ff9dfaab05c
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-24187-7] Audit Policy: Logon-Logoff: Special Logon (Windows Server 2012 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0
```

<span data-ttu-id="c6524-113">Erhalten Sie eine bestimmte Bewertung unter einem bestimmten Steuerelement und standard entsprechend der Bewertungs-ID.</span><span class="sxs-lookup"><span data-stu-id="c6524-113">Get a specific assessment under specific control and standard according to assessment id.</span></span>

### <span data-ttu-id="c6524-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c6524-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplainceAssessment -ResourceId"/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/fe48038b-f73a-4264-b499-0ff9dfaab05c"

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/fe48
                        038b-f73a-4264-b499-0ff9dfaab05c
Name                  : fe48038b-f73a-4264-b499-0ff9dfaab05c
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-24187-7] Audit Policy: Logon-Logoff: Special Logon (Windows Server 2012 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0
```

<span data-ttu-id="c6524-115">Erhalten Sie eine bestimmte Bewertung unter einem bestimmten Steuerelement und standard entsprechend der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c6524-115">Get a specific assessment under specific control and standard according to resource id.</span></span>

## <span data-ttu-id="c6524-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c6524-116">PARAMETERS</span></span>

### <span data-ttu-id="c6524-117">-ControlName</span><span class="sxs-lookup"><span data-stu-id="c6524-117">-ControlName</span></span>
<span data-ttu-id="c6524-118">Steuerelementname.</span><span class="sxs-lookup"><span data-stu-id="c6524-118">Control Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6524-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6524-119">-DefaultProfile</span></span>
<span data-ttu-id="c6524-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6524-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6524-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c6524-121">-Name</span></span>
<span data-ttu-id="c6524-122">Bewertungs-ID.</span><span class="sxs-lookup"><span data-stu-id="c6524-122">Assessment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6524-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6524-123">-ResourceId</span></span>
<span data-ttu-id="c6524-124">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6524-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6524-125">-StandardName</span><span class="sxs-lookup"><span data-stu-id="c6524-125">-StandardName</span></span>
<span data-ttu-id="c6524-126">Standardname.</span><span class="sxs-lookup"><span data-stu-id="c6524-126">Standard Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6524-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6524-127">CommonParameters</span></span>
<span data-ttu-id="c6524-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6524-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6524-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6524-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6524-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6524-130">INPUTS</span></span>

### <span data-ttu-id="c6524-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c6524-131">System.String</span></span>

## <span data-ttu-id="c6524-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6524-132">OUTPUTS</span></span>

### <span data-ttu-id="c6524-133">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceAssessment</span><span class="sxs-lookup"><span data-stu-id="c6524-133">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceAssessment</span></span>

## <span data-ttu-id="c6524-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c6524-134">NOTES</span></span>

## <span data-ttu-id="c6524-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c6524-135">RELATED LINKS</span></span>
