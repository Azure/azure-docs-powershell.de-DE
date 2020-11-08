---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009226"
---
# <span data-ttu-id="2ff58-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2ff58-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="2ff58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ff58-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff58-103">Ruft das Konto ab.</span><span class="sxs-lookup"><span data-stu-id="2ff58-103">Gets the account.</span></span>

## <span data-ttu-id="2ff58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ff58-104">SYNTAX</span></span>

### <span data-ttu-id="2ff58-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ff58-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ff58-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ff58-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ff58-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ff58-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ff58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ff58-108">DESCRIPTION</span></span>
<span data-ttu-id="2ff58-109">Das Get-AzMapsAccount-Cmdlet ruft ein bereitgestelltes Azure Maps-Konto ab, entweder nach Ressourcengruppe und Name oder nach Ressourcen-ID. Darüber hinaus kann Sie eine Liste aller Konten in der ResourceGroup oder alle Azure Maps-Konten für das aktuelle Abonnement zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2ff58-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="2ff58-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ff58-110">EXAMPLES</span></span>

### <span data-ttu-id="2ff58-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ff58-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="2ff58-112">Ruft das Konto mit dem Namen MyAccount in der Ressourcengruppe myresourcegroup ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2ff58-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="2ff58-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2ff58-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="2ff58-114">Ruft alle Azure Maps-Konten in der Ressourcengruppe myresourcegroup ab.</span><span class="sxs-lookup"><span data-stu-id="2ff58-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="2ff58-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2ff58-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="2ff58-116">Ruft alle Azure Maps-Konten im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2ff58-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="2ff58-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="2ff58-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="2ff58-118">Ruft das von der Ressourcen-ID angegebene Kartenkonto ab.</span><span class="sxs-lookup"><span data-stu-id="2ff58-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="2ff58-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ff58-119">PARAMETERS</span></span>

### <span data-ttu-id="2ff58-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff58-120">-DefaultProfile</span></span>
<span data-ttu-id="2ff58-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ff58-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff58-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2ff58-122">-Name</span></span>
<span data-ttu-id="2ff58-123">Ordnet den Kontonamen zu.</span><span class="sxs-lookup"><span data-stu-id="2ff58-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="2ff58-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff58-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ff58-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ff58-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="2ff58-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2ff58-126">-ResourceId</span></span>
<span data-ttu-id="2ff58-127">Maps-Konto-wiederherkunfts-Nr.</span><span class="sxs-lookup"><span data-stu-id="2ff58-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="2ff58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff58-128">CommonParameters</span></span>
<span data-ttu-id="2ff58-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff58-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff58-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff58-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ff58-131">INPUTS</span></span>

### <span data-ttu-id="2ff58-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ff58-132">System.String</span></span>

## <span data-ttu-id="2ff58-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ff58-133">OUTPUTS</span></span>

### <span data-ttu-id="2ff58-134">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2ff58-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="2ff58-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ff58-135">NOTES</span></span>

## <span data-ttu-id="2ff58-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ff58-136">RELATED LINKS</span></span>
