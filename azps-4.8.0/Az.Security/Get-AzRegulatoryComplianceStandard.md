---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174193"
---
# <span data-ttu-id="20f8b-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="20f8b-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="20f8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="20f8b-103">Ruft regulatoey-Konformitätsstandards ab</span><span class="sxs-lookup"><span data-stu-id="20f8b-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="20f8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20f8b-104">SYNTAX</span></span>

### <span data-ttu-id="20f8b-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="20f8b-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20f8b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="20f8b-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20f8b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="20f8b-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20f8b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20f8b-108">DESCRIPTION</span></span>
<span data-ttu-id="20f8b-109">Besorgen Sie sich eine spcific-Compliance-satandard, oder führen Sie alle gesetzlichen Compliance-Standards unter einem bestimmten Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="20f8b-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="20f8b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20f8b-110">EXAMPLES</span></span>

### <span data-ttu-id="20f8b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20f8b-111">Example 1</span></span>
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

<span data-ttu-id="20f8b-112">Besorgen Sie sich alle gesetzlichen Compliance-Standards unter einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20f8b-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="20f8b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="20f8b-113">Example 2</span></span>
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

<span data-ttu-id="20f8b-114">Hier erhalten Sie Informationen zu bestimmten gesetzlichen Compliance-Standards gemäß dem Standardnamen.</span><span class="sxs-lookup"><span data-stu-id="20f8b-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="20f8b-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="20f8b-115">Example 3</span></span>
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

<span data-ttu-id="20f8b-116">Abrufen von Details zu einem bestimmten gesetzlichen Konformitäts Standard entsprechend der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="20f8b-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="20f8b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="20f8b-117">PARAMETERS</span></span>

### <span data-ttu-id="20f8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f8b-118">-DefaultProfile</span></span>
<span data-ttu-id="20f8b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20f8b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20f8b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="20f8b-120">-Name</span></span>
<span data-ttu-id="20f8b-121">Standard Name</span><span class="sxs-lookup"><span data-stu-id="20f8b-121">Standard name.</span></span>

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

### <span data-ttu-id="20f8b-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="20f8b-122">-ResourceId</span></span>
<span data-ttu-id="20f8b-123">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="20f8b-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="20f8b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f8b-124">CommonParameters</span></span>
<span data-ttu-id="20f8b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f8b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f8b-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20f8b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f8b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20f8b-127">INPUTS</span></span>

### <span data-ttu-id="20f8b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="20f8b-128">System.String</span></span>

## <span data-ttu-id="20f8b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20f8b-129">OUTPUTS</span></span>

### <span data-ttu-id="20f8b-130">Microsoft. Azure. Commands. SecurityCenter. Models. RegulatoryCompliance. PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="20f8b-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="20f8b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="20f8b-131">NOTES</span></span>

## <span data-ttu-id="20f8b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20f8b-132">RELATED LINKS</span></span>
