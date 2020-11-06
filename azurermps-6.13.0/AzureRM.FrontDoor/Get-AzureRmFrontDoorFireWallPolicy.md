---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499506"
---
# <span data-ttu-id="271ec-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="271ec-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="271ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="271ec-102">SYNOPSIS</span></span>
<span data-ttu-id="271ec-103">Abrufen der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="271ec-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="271ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="271ec-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="271ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="271ec-105">DESCRIPTION</span></span>
<span data-ttu-id="271ec-106">Die **Get-AzureRmFrontDoorFireWallPolicy-** cmdletGet ruft WAF-Richtlinie in einer Ressourcengruppe unter dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="271ec-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="271ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="271ec-107">EXAMPLES</span></span>

### <span data-ttu-id="271ec-108">Beispiel 1: Abrufen einer WAF-Richtlinie mit dem Namen $Name in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="271ec-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="271ec-109">Abrufen einer WAF-Richtlinie mit dem Namen $Name in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="271ec-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="271ec-110">Beispiel 2: Abrufen aller WAF-Richtlinien in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="271ec-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="271ec-111">Abrufen aller WAF-Richtlinien in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="271ec-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="271ec-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="271ec-112">PARAMETERS</span></span>

### <span data-ttu-id="271ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="271ec-113">-DefaultProfile</span></span>
<span data-ttu-id="271ec-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="271ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271ec-115">-Name</span><span class="sxs-lookup"><span data-stu-id="271ec-115">-Name</span></span>
<span data-ttu-id="271ec-116">FireWallPolicy-Name.</span><span class="sxs-lookup"><span data-stu-id="271ec-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="271ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="271ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="271ec-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="271ec-118">The resource group name.</span></span>

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

### <span data-ttu-id="271ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271ec-119">CommonParameters</span></span>
<span data-ttu-id="271ec-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="271ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271ec-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="271ec-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271ec-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="271ec-122">INPUTS</span></span>

### <span data-ttu-id="271ec-123">System. String</span><span class="sxs-lookup"><span data-stu-id="271ec-123">System.String</span></span>

## <span data-ttu-id="271ec-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="271ec-124">OUTPUTS</span></span>

### <span data-ttu-id="271ec-125">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="271ec-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="271ec-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="271ec-126">NOTES</span></span>

## <span data-ttu-id="271ec-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="271ec-127">RELATED LINKS</span></span>

<span data-ttu-id="271ec-128">[Neu – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Satz-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="271ec-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>
