---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 5933d860ca2badce2d9576409dd1553153bb1e84
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401503"
---
# <span data-ttu-id="4339a-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="4339a-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="4339a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4339a-102">SYNOPSIS</span></span>
<span data-ttu-id="4339a-103">Get WAF policy</span><span class="sxs-lookup"><span data-stu-id="4339a-103">Get WAF policy</span></span>

## <span data-ttu-id="4339a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4339a-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4339a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4339a-105">DESCRIPTION</span></span>
<span data-ttu-id="4339a-106">Das **Cmdlet "Get-AzFrontD selbstFireWallPolicy"** ruft die "WAF-Richtlinie" in einer Ressourcengruppe unter dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="4339a-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="4339a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4339a-107">EXAMPLES</span></span>

### <span data-ttu-id="4339a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4339a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="4339a-109">Sie erhalten eine WAF-Richtlinie namens "$policyName in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4339a-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="4339a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4339a-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="4339a-111">Alle WAF-Richtlinien in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4339a-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="4339a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4339a-112">PARAMETERS</span></span>

### <span data-ttu-id="4339a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4339a-113">-DefaultProfile</span></span>
<span data-ttu-id="4339a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4339a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4339a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4339a-115">-Name</span></span>
<span data-ttu-id="4339a-116">Name von FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="4339a-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4339a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4339a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4339a-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4339a-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4339a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4339a-119">CommonParameters</span></span>
<span data-ttu-id="4339a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4339a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4339a-121">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4339a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4339a-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4339a-122">INPUTS</span></span>

### <span data-ttu-id="4339a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="4339a-123">None</span></span>

## <span data-ttu-id="4339a-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4339a-124">OUTPUTS</span></span>

### <span data-ttu-id="4339a-125">Microsoft.Azure.Commands.FrontD selbst.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="4339a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="4339a-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4339a-126">NOTES</span></span>

## <span data-ttu-id="4339a-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4339a-127">RELATED LINKS</span></span>

<span data-ttu-id="4339a-128">[New-AzFrontD firewallWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontD firewallWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontD firewallWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="4339a-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
