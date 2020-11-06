---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
ms.openlocfilehash: 68ccff91f6e233862ba1ee5aa94a3a3d0d8422b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503582"
---
# <span data-ttu-id="67dc3-101">Get-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="67dc3-101">Get-AzureRmMapsAccount</span></span>

## <span data-ttu-id="67dc3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="67dc3-103">Ruft das Konto ab.</span><span class="sxs-lookup"><span data-stu-id="67dc3-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67dc3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67dc3-104">SYNTAX</span></span>

### <span data-ttu-id="67dc3-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="67dc3-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67dc3-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67dc3-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67dc3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67dc3-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67dc3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67dc3-108">DESCRIPTION</span></span>
<span data-ttu-id="67dc3-109">Das Get-AzureRmMapsAccount-Cmdlet ruft ein bereitgestelltes Azure Maps-Konto ab, entweder nach Ressourcengruppe und Name oder nach Ressourcen-ID. Darüber hinaus kann Sie eine Liste aller Konten in der ResourceGroup oder alle Azure Maps-Konten für das aktuelle Abonnement zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="67dc3-109">The Get-AzureRmMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="67dc3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67dc3-110">EXAMPLES</span></span>

### <span data-ttu-id="67dc3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67dc3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="67dc3-112">Ruft das Konto mit dem Namen MyAccount in der Ressourcengruppe myresourcegroup ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="67dc3-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="67dc3-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="67dc3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="67dc3-114">Ruft alle Azure Maps-Konten in der Ressourcengruppe myresourcegroup ab.</span><span class="sxs-lookup"><span data-stu-id="67dc3-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="67dc3-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="67dc3-115">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="67dc3-116">Ruft alle Azure Maps-Konten im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="67dc3-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="67dc3-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="67dc3-117">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="67dc3-118">Ruft das von der Ressourcen-ID angegebene Kartenkonto ab.</span><span class="sxs-lookup"><span data-stu-id="67dc3-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="67dc3-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="67dc3-119">PARAMETERS</span></span>

### <span data-ttu-id="67dc3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67dc3-120">-DefaultProfile</span></span>
<span data-ttu-id="67dc3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67dc3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67dc3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="67dc3-122">-Name</span></span>
<span data-ttu-id="67dc3-123">Ordnet den Kontonamen zu.</span><span class="sxs-lookup"><span data-stu-id="67dc3-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="67dc3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67dc3-124">-ResourceGroupName</span></span>
<span data-ttu-id="67dc3-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67dc3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="67dc3-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67dc3-126">-ResourceId</span></span>
<span data-ttu-id="67dc3-127">Maps-Konto-wiederherkunfts-Nr.</span><span class="sxs-lookup"><span data-stu-id="67dc3-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="67dc3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67dc3-128">CommonParameters</span></span>
<span data-ttu-id="67dc3-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67dc3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67dc3-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67dc3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67dc3-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67dc3-131">INPUTS</span></span>

### <span data-ttu-id="67dc3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="67dc3-132">System.String</span></span>

## <span data-ttu-id="67dc3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67dc3-133">OUTPUTS</span></span>

### <span data-ttu-id="67dc3-134">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="67dc3-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="67dc3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="67dc3-135">NOTES</span></span>

## <span data-ttu-id="67dc3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67dc3-136">RELATED LINKS</span></span>
