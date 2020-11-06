---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 07bcfff4ab8d1e071ed34c9a52e8aa4e98c32946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480345"
---
# <span data-ttu-id="98c39-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="98c39-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="98c39-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98c39-102">SYNOPSIS</span></span>
<span data-ttu-id="98c39-103">Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="98c39-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="98c39-104">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="98c39-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c39-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98c39-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c39-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98c39-106">DESCRIPTION</span></span>
<span data-ttu-id="98c39-107">Das Cmdlet " **Get-AzureRmDataLakeStoreTrustedIdProvider** " Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="98c39-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="98c39-108">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="98c39-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="98c39-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98c39-109">EXAMPLES</span></span>

### <span data-ttu-id="98c39-110">Beispiel 1: Abrufen eines bestimmten vertrauenswürdigen Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="98c39-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="98c39-111">Gibt den Anbieter mit dem Namen "MyProvider" aus dem Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="98c39-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="98c39-112">Beispiel 2: Auflisten aller Anbieter in einem Konto</span><span class="sxs-lookup"><span data-stu-id="98c39-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="98c39-113">Listet alle Anbieter unter dem Konto "ContosoADL" auf.</span><span class="sxs-lookup"><span data-stu-id="98c39-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="98c39-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="98c39-114">PARAMETERS</span></span>

### <span data-ttu-id="98c39-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="98c39-115">-Account</span></span>
<span data-ttu-id="98c39-116">Das Data Lake Store-Konto zum Abrufen des vertrauenswürdigen Identitätsanbieters aus</span><span class="sxs-lookup"><span data-stu-id="98c39-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="98c39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c39-117">-DefaultProfile</span></span>
<span data-ttu-id="98c39-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="98c39-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98c39-119">-Name</span><span class="sxs-lookup"><span data-stu-id="98c39-119">-Name</span></span>
<span data-ttu-id="98c39-120">Der Name des vertrauenswürdigen Identitätsanbieters, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="98c39-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="98c39-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c39-121">-ResourceGroupName</span></span>
<span data-ttu-id="98c39-122">Der Name der Ressourcengruppe, unter der der angegebene vertrauenswürdige Identitätsanbieter des angegebenen Kontos abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="98c39-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="98c39-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c39-123">CommonParameters</span></span>
<span data-ttu-id="98c39-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c39-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c39-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c39-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c39-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98c39-126">INPUTS</span></span>

### <span data-ttu-id="98c39-127">System. String</span><span class="sxs-lookup"><span data-stu-id="98c39-127">System.String</span></span>

## <span data-ttu-id="98c39-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98c39-128">OUTPUTS</span></span>

### <span data-ttu-id="98c39-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="98c39-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="98c39-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="98c39-130">NOTES</span></span>

## <span data-ttu-id="98c39-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98c39-131">RELATED LINKS</span></span>
