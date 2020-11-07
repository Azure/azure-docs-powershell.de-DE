---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 60d6263d3fb074cf4795379ae28f1824dc81a4c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651133"
---
# <span data-ttu-id="3e1ae-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="3e1ae-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="3e1ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1ae-103">Abrufen der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="3e1ae-103">Get WAF policy</span></span>

## <span data-ttu-id="3e1ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e1ae-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e1ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e1ae-105">DESCRIPTION</span></span>
<span data-ttu-id="3e1ae-106">Die **Get-AzFrontDoorWafPolicy-** cmdletGet ruft WAF-Richtlinie in einer Ressourcengruppe unter dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="3e1ae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e1ae-107">EXAMPLES</span></span>

### <span data-ttu-id="3e1ae-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e1ae-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="3e1ae-109">Abrufen einer WAF-Richtlinie mit dem Namen $policyName in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1ae-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="3e1ae-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3e1ae-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="3e1ae-111">Abrufen aller WAF-Richtlinien in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1ae-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="3e1ae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e1ae-112">PARAMETERS</span></span>

### <span data-ttu-id="3e1ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1ae-113">-DefaultProfile</span></span>
<span data-ttu-id="3e1ae-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e1ae-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3e1ae-115">-Name</span></span>
<span data-ttu-id="3e1ae-116">FireWallPolicy-Name.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="3e1ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e1ae-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-118">The resource group name.</span></span>

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

### <span data-ttu-id="3e1ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1ae-119">CommonParameters</span></span>
<span data-ttu-id="3e1ae-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1ae-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1ae-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e1ae-122">INPUTS</span></span>

### <span data-ttu-id="3e1ae-123">Keine</span><span class="sxs-lookup"><span data-stu-id="3e1ae-123">None</span></span>

## <span data-ttu-id="3e1ae-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e1ae-124">OUTPUTS</span></span>

### <span data-ttu-id="3e1ae-125">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="3e1ae-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="3e1ae-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e1ae-126">NOTES</span></span>

## <span data-ttu-id="3e1ae-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e1ae-127">RELATED LINKS</span></span>

<span data-ttu-id="3e1ae-128">[Neu – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Satz-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3e1ae-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
