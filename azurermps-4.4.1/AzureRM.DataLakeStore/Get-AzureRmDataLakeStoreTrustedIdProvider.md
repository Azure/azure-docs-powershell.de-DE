---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: e95fd5e487fc29a40e48484b0a905def8356e260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501898"
---
# <span data-ttu-id="7ac98-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="7ac98-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="7ac98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ac98-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac98-103">Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="7ac98-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="7ac98-104">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7ac98-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ac98-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ac98-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ac98-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ac98-106">DESCRIPTION</span></span>
<span data-ttu-id="7ac98-107">Das Cmdlet " **Get-AzureRmDataLakeStoreTrustedIdProvider** " Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="7ac98-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="7ac98-108">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7ac98-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="7ac98-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ac98-109">EXAMPLES</span></span>

### <span data-ttu-id="7ac98-110">Beispiel 1: Abrufen eines bestimmten vertrauenswürdigen Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="7ac98-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="7ac98-111">Gibt den Anbieter mit dem Namen "MyProvider" aus dem Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="7ac98-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="7ac98-112">Beispiel 2: Auflisten aller Anbieter in einem Konto</span><span class="sxs-lookup"><span data-stu-id="7ac98-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="7ac98-113">Listet alle Anbieter unter dem Konto "ContosoADL" auf.</span><span class="sxs-lookup"><span data-stu-id="7ac98-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="7ac98-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ac98-114">PARAMETERS</span></span>

### <span data-ttu-id="7ac98-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="7ac98-115">-Account</span></span>
<span data-ttu-id="7ac98-116">Das Data Lake Store-Konto zum Abrufen des vertrauenswürdigen Identitätsanbieters aus</span><span class="sxs-lookup"><span data-stu-id="7ac98-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac98-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7ac98-117">-Name</span></span>
<span data-ttu-id="7ac98-118">Der Name des vertrauenswürdigen Identitätsanbieters, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ac98-118">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ac98-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ac98-120">Der Name der Ressourcengruppe, unter der der angegebene vertrauenswürdige Identitätsanbieter des angegebenen Kontos abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ac98-120">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac98-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac98-121">-DefaultProfile</span></span>
<span data-ttu-id="7ac98-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ac98-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac98-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac98-123">CommonParameters</span></span>
<span data-ttu-id="7ac98-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac98-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac98-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac98-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac98-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ac98-126">INPUTS</span></span>

## <span data-ttu-id="7ac98-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ac98-127">OUTPUTS</span></span>

### <span data-ttu-id="7ac98-128">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="7ac98-128">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="7ac98-129">Die Details des angegebenen vertrauenswürdigen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="7ac98-129">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="7ac98-130">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="7ac98-130">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="7ac98-131">Die Liste der vertrauenswürdigen Identitätsanbieter im angegebenen Konto.</span><span class="sxs-lookup"><span data-stu-id="7ac98-131">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="7ac98-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ac98-132">NOTES</span></span>

## <span data-ttu-id="7ac98-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ac98-133">RELATED LINKS</span></span>

