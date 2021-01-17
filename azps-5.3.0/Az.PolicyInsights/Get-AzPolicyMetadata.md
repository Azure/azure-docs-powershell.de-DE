---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459791"
---
# <span data-ttu-id="7bac5-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="7bac5-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="7bac5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bac5-102">SYNOPSIS</span></span>
<span data-ttu-id="7bac5-103">Ruft Richtlinienmetadatenressourcen ab</span><span class="sxs-lookup"><span data-stu-id="7bac5-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="7bac5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bac5-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7bac5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bac5-105">DESCRIPTION</span></span>
<span data-ttu-id="7bac5-106">Das **Cmdlet "Get-AzPolicyRemediation"** ruft alle Metadatenressourcen für Richtlinien oder eine bestimmte Metadatenressource für Richtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="7bac5-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="7bac5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7bac5-107">EXAMPLES</span></span>

### <span data-ttu-id="7bac5-108">Beispiel 1: Alle Metadatenressourcen für Richtlinien erhalten</span><span class="sxs-lookup"><span data-stu-id="7bac5-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="7bac5-109">Dieser Befehl ruft alle Metadatenressourcen für Richtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="7bac5-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="7bac5-110">Beispiel 2: Erhalten einer Sammlung von 10 Ressourcen für Richtlinienmetadaten</span><span class="sxs-lookup"><span data-stu-id="7bac5-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="7bac5-111">Dieser Befehl ruft eine Sammlung von 10 Ressourcen für Richtlinienmetadaten ab.</span><span class="sxs-lookup"><span data-stu-id="7bac5-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="7bac5-112">Beispiel 3: Erhalten einer einzelnen Metadatenressource für Richtlinien mit dem Namen 'ACF1348'</span><span class="sxs-lookup"><span data-stu-id="7bac5-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="7bac5-113">Dieser Befehl ruft eine einzelne Metadatenressource für Richtlinien mit dem Namen 'ACF1348' ab.</span><span class="sxs-lookup"><span data-stu-id="7bac5-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="7bac5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bac5-114">PARAMETERS</span></span>

### <span data-ttu-id="7bac5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bac5-115">-DefaultProfile</span></span>
<span data-ttu-id="7bac5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bac5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bac5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7bac5-117">-Name</span></span>
<span data-ttu-id="7bac5-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7bac5-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bac5-119">-Top</span><span class="sxs-lookup"><span data-stu-id="7bac5-119">-Top</span></span>
<span data-ttu-id="7bac5-120">Maximale Anzahl von Zurücksendungsressourcen für Richtlinienmetadaten.</span><span class="sxs-lookup"><span data-stu-id="7bac5-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bac5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bac5-121">CommonParameters</span></span>
<span data-ttu-id="7bac5-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bac5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bac5-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bac5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bac5-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7bac5-124">INPUTS</span></span>

### <span data-ttu-id="7bac5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="7bac5-125">System.String</span></span>

## <span data-ttu-id="7bac5-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7bac5-126">OUTPUTS</span></span>

### <span data-ttu-id="7bac5-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="7bac5-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="7bac5-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7bac5-128">NOTES</span></span>

## <span data-ttu-id="7bac5-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7bac5-129">RELATED LINKS</span></span>
