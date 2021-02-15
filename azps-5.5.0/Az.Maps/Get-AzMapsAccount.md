---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159484"
---
# <span data-ttu-id="682f5-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="682f5-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="682f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="682f5-102">SYNOPSIS</span></span>
<span data-ttu-id="682f5-103">Ruft das Konto ab.</span><span class="sxs-lookup"><span data-stu-id="682f5-103">Gets the account.</span></span>

## <span data-ttu-id="682f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="682f5-104">SYNTAX</span></span>

### <span data-ttu-id="682f5-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="682f5-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="682f5-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="682f5-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="682f5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="682f5-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="682f5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="682f5-108">DESCRIPTION</span></span>
<span data-ttu-id="682f5-109">Das Get-AzMapsAccount erhält ein bereitgestelltes Azure Maps-Konto, entweder nach Ressourcengruppe und -name oder nach Ressourcen-ID. Darüber hinaus kann sie eine Liste aller Konten in der Ressourcengruppe oder alle Azure Maps-Konten für das aktuelle Abonnement zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="682f5-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="682f5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="682f5-110">EXAMPLES</span></span>

### <span data-ttu-id="682f5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="682f5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="682f5-112">Ruft das Konto mit dem Namen "MyAccount" in der Ressourcengruppe "MyResourceGroup" ab, sofern es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="682f5-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="682f5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="682f5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="682f5-114">Ruft alle Azure -Karten-Konten in der Ressourcengruppe "MyResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="682f5-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="682f5-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="682f5-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="682f5-116">Ruft alle Azure -Karten-Konten im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="682f5-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="682f5-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="682f5-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="682f5-118">Ruft das Kartenkonto ab, das durch die Ressourcen-ID angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="682f5-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="682f5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="682f5-119">PARAMETERS</span></span>

### <span data-ttu-id="682f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="682f5-120">-DefaultProfile</span></span>
<span data-ttu-id="682f5-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="682f5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="682f5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="682f5-122">-Name</span></span>
<span data-ttu-id="682f5-123">Kartenkontoname.</span><span class="sxs-lookup"><span data-stu-id="682f5-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="682f5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="682f5-124">-ResourceGroupName</span></span>
<span data-ttu-id="682f5-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="682f5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="682f5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="682f5-126">-ResourceId</span></span>
<span data-ttu-id="682f5-127">Karten "Account ResourceId".</span><span class="sxs-lookup"><span data-stu-id="682f5-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="682f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="682f5-128">CommonParameters</span></span>
<span data-ttu-id="682f5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="682f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="682f5-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="682f5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="682f5-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="682f5-131">INPUTS</span></span>

### <span data-ttu-id="682f5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="682f5-132">System.String</span></span>

## <span data-ttu-id="682f5-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="682f5-133">OUTPUTS</span></span>

### <span data-ttu-id="682f5-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="682f5-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="682f5-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="682f5-135">NOTES</span></span>

## <span data-ttu-id="682f5-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="682f5-136">RELATED LINKS</span></span>
