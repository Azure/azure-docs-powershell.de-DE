---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 83f2c49eb696ac4e3fef0f411b79af24ae95f56c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919960"
---
# <span data-ttu-id="ddea2-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="ddea2-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="ddea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddea2-102">SYNOPSIS</span></span>
<span data-ttu-id="ddea2-103">WaF-Richtlinie erhalten</span><span class="sxs-lookup"><span data-stu-id="ddea2-103">Get WAF policy</span></span>

## <span data-ttu-id="ddea2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddea2-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddea2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddea2-105">DESCRIPTION</span></span>
<span data-ttu-id="ddea2-106">Das **Get-AzFrontDoorWafPolicy-CmdletGet** ruft die WAF-Richtlinie in einer Ressourcengruppe unter dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ddea2-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="ddea2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddea2-107">EXAMPLES</span></span>

### <span data-ttu-id="ddea2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddea2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="ddea2-109">Eine WAF-Richtlinie namens $policyName in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddea2-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="ddea2-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ddea2-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="ddea2-111">Alle WAF-Richtlinien in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddea2-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="ddea2-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ddea2-112">PARAMETERS</span></span>

### <span data-ttu-id="ddea2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddea2-113">-DefaultProfile</span></span>
<span data-ttu-id="ddea2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddea2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddea2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ddea2-115">-Name</span></span>
<span data-ttu-id="ddea2-116">Name von FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="ddea2-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="ddea2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddea2-117">-ResourceGroupName</span></span>
<span data-ttu-id="ddea2-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddea2-118">The resource group name.</span></span>

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

### <span data-ttu-id="ddea2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddea2-119">CommonParameters</span></span>
<span data-ttu-id="ddea2-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddea2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddea2-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddea2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddea2-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddea2-122">INPUTS</span></span>

### <span data-ttu-id="ddea2-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ddea2-123">None</span></span>

## <span data-ttu-id="ddea2-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddea2-124">OUTPUTS</span></span>

### <span data-ttu-id="ddea2-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ddea2-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="ddea2-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ddea2-126">NOTES</span></span>

## <span data-ttu-id="ddea2-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ddea2-127">RELATED LINKS</span></span>

<span data-ttu-id="ddea2-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="ddea2-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
