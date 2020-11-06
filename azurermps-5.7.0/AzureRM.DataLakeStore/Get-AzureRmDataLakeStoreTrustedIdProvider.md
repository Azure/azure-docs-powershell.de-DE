---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c387ebb089ab7f9dfddaee818f26596f34ed91e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503777"
---
# <span data-ttu-id="e139f-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="e139f-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="e139f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e139f-102">SYNOPSIS</span></span>
<span data-ttu-id="e139f-103">Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="e139f-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="e139f-104">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e139f-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e139f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e139f-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e139f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e139f-106">DESCRIPTION</span></span>
<span data-ttu-id="e139f-107">Das Cmdlet " **Get-AzureRmDataLakeStoreTrustedIdProvider** " Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="e139f-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="e139f-108">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e139f-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="e139f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e139f-109">EXAMPLES</span></span>

### <span data-ttu-id="e139f-110">Beispiel 1: Abrufen eines bestimmten vertrauenswürdigen Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="e139f-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="e139f-111">Gibt den Anbieter mit dem Namen "MyProvider" aus dem Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="e139f-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="e139f-112">Beispiel 2: Auflisten aller Anbieter in einem Konto</span><span class="sxs-lookup"><span data-stu-id="e139f-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="e139f-113">Listet alle Anbieter unter dem Konto "ContosoADL" auf.</span><span class="sxs-lookup"><span data-stu-id="e139f-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="e139f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e139f-114">PARAMETERS</span></span>

### <span data-ttu-id="e139f-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="e139f-115">-Account</span></span>
<span data-ttu-id="e139f-116">Das Data Lake Store-Konto zum Abrufen des vertrauenswürdigen Identitätsanbieters aus</span><span class="sxs-lookup"><span data-stu-id="e139f-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e139f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e139f-117">-DefaultProfile</span></span>
<span data-ttu-id="e139f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e139f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e139f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e139f-119">-Name</span></span>
<span data-ttu-id="e139f-120">Der Name des vertrauenswürdigen Identitätsanbieters, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e139f-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e139f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e139f-121">-ResourceGroupName</span></span>
<span data-ttu-id="e139f-122">Der Name der Ressourcengruppe, unter der der angegebene vertrauenswürdige Identitätsanbieter des angegebenen Kontos abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e139f-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e139f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e139f-123">CommonParameters</span></span>
<span data-ttu-id="e139f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e139f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e139f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e139f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e139f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e139f-126">INPUTS</span></span>

### <span data-ttu-id="e139f-127">Keine</span><span class="sxs-lookup"><span data-stu-id="e139f-127">None</span></span>
<span data-ttu-id="e139f-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e139f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e139f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e139f-129">OUTPUTS</span></span>

### <span data-ttu-id="e139f-130">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="e139f-130">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="e139f-131">Die Details des angegebenen vertrauenswürdigen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="e139f-131">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="e139f-132">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="e139f-132">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="e139f-133">Die Liste der vertrauenswürdigen Identitätsanbieter im angegebenen Konto.</span><span class="sxs-lookup"><span data-stu-id="e139f-133">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="e139f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="e139f-134">NOTES</span></span>

## <span data-ttu-id="e139f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e139f-135">RELATED LINKS</span></span>

