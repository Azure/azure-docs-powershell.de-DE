---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: c13b4ed784f37e9b01bc8cf5dd618d97305a95d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946912"
---
# <span data-ttu-id="a8295-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="a8295-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="a8295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8295-102">SYNOPSIS</span></span>
<span data-ttu-id="a8295-103">Ruft Richtlinien für Compliancestandards ab</span><span class="sxs-lookup"><span data-stu-id="a8295-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="a8295-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8295-104">SYNTAX</span></span>

### <span data-ttu-id="a8295-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8295-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8295-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a8295-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8295-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8295-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8295-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8295-108">DESCRIPTION</span></span>
<span data-ttu-id="a8295-109">Erhalten Sie eine spcific regulatory compliance , oder listen Sie alle gesetzlichen Compliancestandards unter einem bestimmten Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="a8295-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="a8295-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a8295-110">EXAMPLES</span></span>

### <span data-ttu-id="a8295-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8295-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="a8295-112">Holen Sie sich alle gesetzlichen Compliancestandards unter einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8295-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="a8295-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a8295-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="a8295-114">Hier erhalten Sie Details zu einem bestimmten Gesetzlichen Compliancestandard entsprechend dem Standardnamen.</span><span class="sxs-lookup"><span data-stu-id="a8295-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="a8295-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a8295-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="a8295-116">Erhalten Sie Details zu bestimmten gesetzlichen Compliancestandards entsprechend der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a8295-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="a8295-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a8295-117">PARAMETERS</span></span>

### <span data-ttu-id="a8295-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8295-118">-DefaultProfile</span></span>
<span data-ttu-id="a8295-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8295-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8295-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a8295-120">-Name</span></span>
<span data-ttu-id="a8295-121">Standardname.</span><span class="sxs-lookup"><span data-stu-id="a8295-121">Standard name.</span></span>

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

### <span data-ttu-id="a8295-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8295-122">-ResourceId</span></span>
<span data-ttu-id="a8295-123">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="a8295-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a8295-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8295-124">CommonParameters</span></span>
<span data-ttu-id="a8295-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8295-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8295-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8295-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8295-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a8295-127">INPUTS</span></span>

### <span data-ttu-id="a8295-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a8295-128">System.String</span></span>

## <span data-ttu-id="a8295-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a8295-129">OUTPUTS</span></span>

### <span data-ttu-id="a8295-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="a8295-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="a8295-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a8295-131">NOTES</span></span>

## <span data-ttu-id="a8295-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a8295-132">RELATED LINKS</span></span>
