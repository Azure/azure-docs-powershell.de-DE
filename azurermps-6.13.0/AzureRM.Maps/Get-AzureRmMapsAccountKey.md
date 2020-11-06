---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497357"
---
# <span data-ttu-id="2fabb-101">Get-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="2fabb-101">Get-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="2fabb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fabb-102">SYNOPSIS</span></span>
<span data-ttu-id="2fabb-103">Ruft die API-Schlüssel für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="2fabb-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="2fabb-104">Diese Schlüssel sind der Authentifizierungsmechanismus, der bei nachfolgenden Aufrufen von Azure Maps verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2fabb-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fabb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fabb-105">SYNTAX</span></span>

### <span data-ttu-id="2fabb-106">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fabb-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fabb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fabb-107">InputObjectParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fabb-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fabb-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fabb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fabb-109">DESCRIPTION</span></span>
<span data-ttu-id="2fabb-110">Das Get-AzureRmMapsAccountKey-Cmdlet ruft die API-Schlüssel für ein bereitgestelltes Azure Maps-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="2fabb-110">The Get-AzureRmMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="2fabb-111">Ein Azure Maps-Konto verfügt über zwei API-Schlüssel: primäre und sekundäre.</span><span class="sxs-lookup"><span data-stu-id="2fabb-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="2fabb-112">Die Tasten ermöglichen die Interaktion mit dem Azure Maps-Konto Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="2fabb-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="2fabb-113">Verwenden Sie New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey. MD), um einen Schlüssel neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="2fabb-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="2fabb-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fabb-114">EXAMPLES</span></span>

### <span data-ttu-id="2fabb-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fabb-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="2fabb-116">Gibt die Schlüssel für das Konto mit dem Namen MyAccount in der Ressourcengruppe myresourcegroup zurück.</span><span class="sxs-lookup"><span data-stu-id="2fabb-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="2fabb-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2fabb-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="2fabb-118">Gibt die Schlüssel für das angegebene Azure Maps-Konto zurück.</span><span class="sxs-lookup"><span data-stu-id="2fabb-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="2fabb-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fabb-119">PARAMETERS</span></span>

### <span data-ttu-id="2fabb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fabb-120">-DefaultProfile</span></span>
<span data-ttu-id="2fabb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2fabb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fabb-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2fabb-122">-InputObject</span></span>
<span data-ttu-id="2fabb-123">Kartenkonto, das von Get-AzureRmMapsAccount umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2fabb-123">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fabb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2fabb-124">-Name</span></span>
<span data-ttu-id="2fabb-125">Ordnet den Kontonamen zu.</span><span class="sxs-lookup"><span data-stu-id="2fabb-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fabb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fabb-126">-ResourceGroupName</span></span>
<span data-ttu-id="2fabb-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2fabb-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fabb-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2fabb-128">-ResourceId</span></span>
<span data-ttu-id="2fabb-129">Maps-Konto-wiederherkunfts-Nr.</span><span class="sxs-lookup"><span data-stu-id="2fabb-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="2fabb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fabb-130">CommonParameters</span></span>
<span data-ttu-id="2fabb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fabb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fabb-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fabb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fabb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fabb-133">INPUTS</span></span>

### <span data-ttu-id="2fabb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2fabb-134">System.String</span></span>

### <span data-ttu-id="2fabb-135">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2fabb-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="2fabb-136">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2fabb-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2fabb-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fabb-137">OUTPUTS</span></span>

### <span data-ttu-id="2fabb-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2fabb-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="2fabb-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fabb-139">NOTES</span></span>

## <span data-ttu-id="2fabb-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fabb-140">RELATED LINKS</span></span>
