---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: 11c6c1073f53ba4a4b93fdae02ae6f6eb22e0f04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293009"
---
# <span data-ttu-id="7c00f-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="7c00f-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="7c00f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c00f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c00f-103">Erhält Steuerelemente zur Einhaltung gesetzlicher Vorschriften</span><span class="sxs-lookup"><span data-stu-id="7c00f-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="7c00f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c00f-104">SYNTAX</span></span>

### <span data-ttu-id="7c00f-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c00f-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c00f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c00f-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c00f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c00f-107">DESCRIPTION</span></span>
<span data-ttu-id="7c00f-108">Erhalten Sie spezifische Steuerelementdetails, oder listen Sie alle Steuerelemente unter einem bestimmten Gesetzlichen Compliancestandard auf.</span><span class="sxs-lookup"><span data-stu-id="7c00f-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="7c00f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c00f-109">EXAMPLES</span></span>

### <span data-ttu-id="7c00f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c00f-110">Example 1</span></span>
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

<span data-ttu-id="7c00f-111">Erhalten Sie alle Steuerelemente unter bestimmten gesetzlichen Vorschriften.</span><span class="sxs-lookup"><span data-stu-id="7c00f-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="7c00f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7c00f-112">Example 2</span></span>
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

<span data-ttu-id="7c00f-113">Erhalten Sie spezifische Steuerelementdetails entsprechend der Steuerelement-ID.</span><span class="sxs-lookup"><span data-stu-id="7c00f-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="7c00f-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7c00f-114">Example 3</span></span>
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

<span data-ttu-id="7c00f-115">Erhalten Sie spezifische Steuerelementdetails entsprechend der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7c00f-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="7c00f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c00f-116">PARAMETERS</span></span>

### <span data-ttu-id="7c00f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c00f-117">-DefaultProfile</span></span>
<span data-ttu-id="7c00f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c00f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c00f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7c00f-119">-Name</span></span>
<span data-ttu-id="7c00f-120">Steuerelement-ID.</span><span class="sxs-lookup"><span data-stu-id="7c00f-120">Control Id.</span></span>

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

### <span data-ttu-id="7c00f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c00f-121">-ResourceId</span></span>
<span data-ttu-id="7c00f-122">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="7c00f-122">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="7c00f-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="7c00f-123">-StandardName</span></span>
<span data-ttu-id="7c00f-124">Standardname.</span><span class="sxs-lookup"><span data-stu-id="7c00f-124">Standard Name.</span></span>

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

### <span data-ttu-id="7c00f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c00f-125">CommonParameters</span></span>
<span data-ttu-id="7c00f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c00f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c00f-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c00f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c00f-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c00f-128">INPUTS</span></span>

### <span data-ttu-id="7c00f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7c00f-129">System.String</span></span>

## <span data-ttu-id="7c00f-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c00f-130">OUTPUTS</span></span>

### <span data-ttu-id="7c00f-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="7c00f-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="7c00f-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c00f-132">NOTES</span></span>

## <span data-ttu-id="7c00f-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c00f-133">RELATED LINKS</span></span>
