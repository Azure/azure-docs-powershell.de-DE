---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504541"
---
# <span data-ttu-id="008d1-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="008d1-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="008d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="008d1-102">SYNOPSIS</span></span>
<span data-ttu-id="008d1-103">Ruft die API-Schlüssel für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="008d1-103">Gets the API keys for an account.</span></span> <span data-ttu-id="008d1-104">Diese Schlüssel sind der Authentifizierungsmechanismus, der bei nachfolgenden Aufrufen von Azure Location based Services verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="008d1-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="008d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="008d1-105">SYNTAX</span></span>

### <span data-ttu-id="008d1-106">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="008d1-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008d1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="008d1-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008d1-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="008d1-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="008d1-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="008d1-109">DESCRIPTION</span></span>
<span data-ttu-id="008d1-110">Das Cmdlet " **Get-AzureRmLocationBasedServicesAccountKey** " Ruft die API-Schlüssel für ein bereitgestelltes standortbasiertes Dienstkonto ab.</span><span class="sxs-lookup"><span data-stu-id="008d1-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="008d1-111">Ein standortbasiertes Dienstkonto verfügt über zwei API-Schlüssel: primäre und sekundäre.</span><span class="sxs-lookup"><span data-stu-id="008d1-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="008d1-112">Die Tasten ermöglichen die Interaktion mit dem Endpunkt des standortbasierten Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="008d1-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="008d1-113">Verwenden Sie [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) , um einen Schlüssel neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="008d1-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="008d1-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="008d1-114">EXAMPLES</span></span>

### <span data-ttu-id="008d1-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="008d1-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="008d1-116">Gibt die Schlüssel für das Konto mit dem Namen MyAccount in der Ressourcengruppe myresourcegroup zurück.</span><span class="sxs-lookup"><span data-stu-id="008d1-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="008d1-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="008d1-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="008d1-118">Gibt die Schlüssel für das angegebene Location based Services-Konto zurück.</span><span class="sxs-lookup"><span data-stu-id="008d1-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="008d1-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="008d1-119">PARAMETERS</span></span>

### <span data-ttu-id="008d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008d1-120">-DefaultProfile</span></span>
<span data-ttu-id="008d1-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="008d1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008d1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="008d1-122">-InputObject</span></span>
<span data-ttu-id="008d1-123">Standortbasiertes Dienstkonto, piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="008d1-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="008d1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="008d1-124">-Name</span></span>
<span data-ttu-id="008d1-125">Name des standortbasierten Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="008d1-125">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008d1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="008d1-126">-ResourceGroupName</span></span>
<span data-ttu-id="008d1-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="008d1-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008d1-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="008d1-128">-ResourceId</span></span>
<span data-ttu-id="008d1-129">Location based Services-Konto-Resourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="008d1-129">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008d1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008d1-130">CommonParameters</span></span>
<span data-ttu-id="008d1-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008d1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008d1-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="008d1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008d1-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="008d1-133">INPUTS</span></span>

### <span data-ttu-id="008d1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="008d1-134">System.String</span></span>

## <span data-ttu-id="008d1-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="008d1-135">OUTPUTS</span></span>

### <span data-ttu-id="008d1-136">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="008d1-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="008d1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008d1-137">CommonParameters</span></span>
<span data-ttu-id="008d1-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008d1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008d1-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="008d1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008d1-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="008d1-140">NOTES</span></span>

## <span data-ttu-id="008d1-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="008d1-141">RELATED LINKS</span></span>
