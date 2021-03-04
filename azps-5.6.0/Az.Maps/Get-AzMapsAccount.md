---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: 420cf84bb946df3d7f2110937aa332e25978aa8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940419"
---
# <span data-ttu-id="e8678-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e8678-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="e8678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8678-102">SYNOPSIS</span></span>
<span data-ttu-id="e8678-103">Ruft das Konto ab.</span><span class="sxs-lookup"><span data-stu-id="e8678-103">Gets the account.</span></span>

## <span data-ttu-id="e8678-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8678-104">SYNTAX</span></span>

### <span data-ttu-id="e8678-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8678-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8678-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8678-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8678-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8678-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8678-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8678-108">DESCRIPTION</span></span>
<span data-ttu-id="e8678-109">Das Get-AzMapsAccount-Cmdlet erhält ein bereitgestelltes Azure Maps-Konto, entweder nach Ressourcengruppe und -name oder nach Ressourcen-ID. Darüber hinaus kann sie eine Liste aller Konten in der Ressourcengruppe oder aller Azure Maps-Konten für das aktuelle Abonnement zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e8678-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="e8678-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8678-110">EXAMPLES</span></span>

### <span data-ttu-id="e8678-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8678-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="e8678-112">Ruft das Konto mit dem Namen MyAccount in der Ressourcengruppe MyResourceGroup ab, sofern es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e8678-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="e8678-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e8678-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="e8678-114">Ruft alle Azure Maps-Konten in der Ressourcengruppe MyResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="e8678-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e8678-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e8678-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="e8678-116">Ruft alle Azure Maps-Konten im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e8678-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="e8678-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e8678-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="e8678-118">Ruft das mit der Ressourcen-ID angegebene Kartenkonto ab.</span><span class="sxs-lookup"><span data-stu-id="e8678-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="e8678-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e8678-119">PARAMETERS</span></span>

### <span data-ttu-id="e8678-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8678-120">-DefaultProfile</span></span>
<span data-ttu-id="e8678-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8678-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8678-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e8678-122">-Name</span></span>
<span data-ttu-id="e8678-123">Karten-Kontoname.</span><span class="sxs-lookup"><span data-stu-id="e8678-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8678-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8678-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8678-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e8678-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8678-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8678-126">-ResourceId</span></span>
<span data-ttu-id="e8678-127">Ordnet "Account ResourceId" zu.</span><span class="sxs-lookup"><span data-stu-id="e8678-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8678-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8678-128">CommonParameters</span></span>
<span data-ttu-id="e8678-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8678-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8678-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8678-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8678-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8678-131">INPUTS</span></span>

### <span data-ttu-id="e8678-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e8678-132">System.String</span></span>

## <span data-ttu-id="e8678-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8678-133">OUTPUTS</span></span>

### <span data-ttu-id="e8678-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e8678-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="e8678-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e8678-135">NOTES</span></span>

## <span data-ttu-id="e8678-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e8678-136">RELATED LINKS</span></span>
