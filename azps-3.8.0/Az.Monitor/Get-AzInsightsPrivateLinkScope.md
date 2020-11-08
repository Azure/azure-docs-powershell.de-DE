---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004293"
---
# <span data-ttu-id="a5e2d-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a5e2d-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="a5e2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e2d-103">Bereich "privaten Link abrufen"</span><span class="sxs-lookup"><span data-stu-id="a5e2d-103">Get private link scope</span></span>

## <span data-ttu-id="a5e2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5e2d-104">SYNTAX</span></span>

### <span data-ttu-id="a5e2d-105">ByResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5e2d-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5e2d-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e2d-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5e2d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e2d-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5e2d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5e2d-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e2d-109">Bereich "Liste" oder "privaten Link abrufen"</span><span class="sxs-lookup"><span data-stu-id="a5e2d-109">List or get private link scope</span></span> 

## <span data-ttu-id="a5e2d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5e2d-110">EXAMPLES</span></span>

### <span data-ttu-id="a5e2d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5e2d-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="a5e2d-112">Auflisten privater Verknüpfungs Bereiche unter Ressourcengruppe "rg_name"</span><span class="sxs-lookup"><span data-stu-id="a5e2d-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="a5e2d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a5e2d-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="a5e2d-114">Abrufen des Bereichs für private Links mit dem Namen "scope_name" unter Ressourcengruppe "rg_name"</span><span class="sxs-lookup"><span data-stu-id="a5e2d-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="a5e2d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5e2d-115">PARAMETERS</span></span>

### <span data-ttu-id="a5e2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e2d-116">-DefaultProfile</span></span>
<span data-ttu-id="a5e2d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5e2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e2d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a5e2d-118">-Name</span></span>
<span data-ttu-id="a5e2d-119">Name des privaten Link Bereichs</span><span class="sxs-lookup"><span data-stu-id="a5e2d-119">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e2d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e2d-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5e2d-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a5e2d-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e2d-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a5e2d-122">-ResourceId</span></span>
<span data-ttu-id="a5e2d-123">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a5e2d-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e2d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e2d-124">CommonParameters</span></span>
<span data-ttu-id="a5e2d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e2d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e2d-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5e2d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e2d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5e2d-127">INPUTS</span></span>

### <span data-ttu-id="a5e2d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e2d-128">System.String</span></span>

## <span data-ttu-id="a5e2d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5e2d-129">OUTPUTS</span></span>

### <span data-ttu-id="a5e2d-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a5e2d-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="a5e2d-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5e2d-131">NOTES</span></span>

## <span data-ttu-id="a5e2d-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5e2d-132">RELATED LINKS</span></span>
