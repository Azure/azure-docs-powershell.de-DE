---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: b6c0a8540c08d4bf723886878b7055201aaa6922
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927568"
---
# <span data-ttu-id="f6f7d-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="f6f7d-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="f6f7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f7d-103">Ruft gesetzliche Compliancesteuerelemente ab</span><span class="sxs-lookup"><span data-stu-id="f6f7d-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="f6f7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6f7d-104">SYNTAX</span></span>

### <span data-ttu-id="f6f7d-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6f7d-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6f7d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6f7d-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6f7d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6f7d-107">DESCRIPTION</span></span>
<span data-ttu-id="f6f7d-108">Erhalten Sie spezifische Steuerelementdetails, oder listen Sie alle Steuerelemente unter einem bestimmten gesetzlichen Compliancestandard auf.</span><span class="sxs-lookup"><span data-stu-id="f6f7d-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="f6f7d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6f7d-109">EXAMPLES</span></span>

### <span data-ttu-id="f6f7d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6f7d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.1
Name               : A1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Current processing capacity and usage are maintained, monitored, and evaluated to manage capacity
                     demand and to enable the implementation of additional capacity to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.2
Name               : A1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Environmental protections, software, data backup processes, and recovery infrastructure are
                     designed, developed, implemented, operated, maintained, and monitored to meet availability
                     commitments and requirements.
State              : Passed
PassedAssessments  : 3
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.3
Name               : A1.3
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Recovery plan procedures supporting system recovery are tested to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.1
Name               : C1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information is protected during the system design, development, testing,
                     implementation, and change processes in accordance with confidentiality commitments and
                     requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0
```

<span data-ttu-id="f6f7d-111">Holen Sie sich alle Steuerelemente unter einem bestimmten gesetzlichen Standard.</span><span class="sxs-lookup"><span data-stu-id="f6f7d-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="f6f7d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f6f7d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP" -Name "C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="f6f7d-113">Erhalten Sie bestimmte Steuerelementdetails entsprechend der Steuerelement-ID.</span><span class="sxs-lookup"><span data-stu-id="f6f7d-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="f6f7d-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f6f7d-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="f6f7d-115">Holen Sie sich bestimmte Steuerelementdetails entsprechend der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f6f7d-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="f6f7d-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f6f7d-116">PARAMETERS</span></span>

### <span data-ttu-id="f6f7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f7d-117">-DefaultProfile</span></span>
<span data-ttu-id="f6f7d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6f7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6f7d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f6f7d-119">-Name</span></span>
<span data-ttu-id="f6f7d-120">Steuerelement-ID.</span><span class="sxs-lookup"><span data-stu-id="f6f7d-120">Control Id.</span></span>

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

### <span data-ttu-id="f6f7d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6f7d-121">-ResourceId</span></span>
<span data-ttu-id="f6f7d-122">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="f6f7d-122">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f6f7d-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="f6f7d-123">-StandardName</span></span>
<span data-ttu-id="f6f7d-124">Standardname.</span><span class="sxs-lookup"><span data-stu-id="f6f7d-124">Standard Name.</span></span>

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

### <span data-ttu-id="f6f7d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f7d-125">CommonParameters</span></span>
<span data-ttu-id="f6f7d-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f7d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f7d-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6f7d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f7d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6f7d-128">INPUTS</span></span>

### <span data-ttu-id="f6f7d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f6f7d-129">System.String</span></span>

## <span data-ttu-id="f6f7d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6f7d-130">OUTPUTS</span></span>

### <span data-ttu-id="f6f7d-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="f6f7d-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="f6f7d-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f6f7d-132">NOTES</span></span>

## <span data-ttu-id="f6f7d-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f6f7d-133">RELATED LINKS</span></span>
