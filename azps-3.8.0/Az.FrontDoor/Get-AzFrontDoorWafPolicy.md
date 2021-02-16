---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: daf4631041093b10a1bf712649de8b5c3ad3b6d9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404019"
---
# <span data-ttu-id="670bc-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="670bc-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="670bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="670bc-102">SYNOPSIS</span></span>
<span data-ttu-id="670bc-103">Holen Sie sich die WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="670bc-103">Get WAF policy</span></span>

## <span data-ttu-id="670bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="670bc-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="670bc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="670bc-105">DESCRIPTION</span></span>
<span data-ttu-id="670bc-106">Das **Cmdlet "Get-AzFrontDlicWafPolicy"** ruft die "WAF-Richtlinie" in einer Ressourcengruppe unter dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="670bc-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="670bc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="670bc-107">EXAMPLES</span></span>

### <span data-ttu-id="670bc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="670bc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="670bc-109">Sie erhalten eine WAF-Richtlinie namens "$policyName in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670bc-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="670bc-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="670bc-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="670bc-111">Alle WAF-Richtlinien in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670bc-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="670bc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="670bc-112">PARAMETERS</span></span>

### <span data-ttu-id="670bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670bc-113">-DefaultProfile</span></span>
<span data-ttu-id="670bc-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="670bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="670bc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="670bc-115">-Name</span></span>
<span data-ttu-id="670bc-116">Name von FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="670bc-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="670bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="670bc-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="670bc-118">The resource group name.</span></span>

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

### <span data-ttu-id="670bc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670bc-119">CommonParameters</span></span>
<span data-ttu-id="670bc-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670bc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670bc-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="670bc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670bc-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="670bc-122">INPUTS</span></span>

### <span data-ttu-id="670bc-123">Keine</span><span class="sxs-lookup"><span data-stu-id="670bc-123">None</span></span>

## <span data-ttu-id="670bc-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="670bc-124">OUTPUTS</span></span>

### <span data-ttu-id="670bc-125">Microsoft.Azure.Commands.FrontDando.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="670bc-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="670bc-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="670bc-126">NOTES</span></span>

## <span data-ttu-id="670bc-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="670bc-127">RELATED LINKS</span></span>

<span data-ttu-id="670bc-128">[New-AzFrontDlicWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDlicWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDlicWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="670bc-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
