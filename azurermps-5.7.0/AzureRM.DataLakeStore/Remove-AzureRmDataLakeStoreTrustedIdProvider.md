---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c769e3e084f0ac5fd6df22bae81a4d8df99dc700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504578"
---
# <span data-ttu-id="06cde-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="06cde-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="06cde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06cde-102">SYNOPSIS</span></span>
<span data-ttu-id="06cde-103">Entfernt den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="06cde-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06cde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06cde-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06cde-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06cde-105">DESCRIPTION</span></span>
<span data-ttu-id="06cde-106">Mit dem Cmdlet **Remove-AzureRmDataLakeStoreTrustedIdProvider** wird der angegebene Trusted Identity-Anbieter im angegebenen Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="06cde-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="06cde-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06cde-107">EXAMPLES</span></span>

### <span data-ttu-id="06cde-108">Beispiel 1: Entfernen Sie einen vertrauenswürdigen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="06cde-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="06cde-109">Entfernt den Anbieter "MyProvider" aus dem Konto "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="06cde-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="06cde-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="06cde-110">PARAMETERS</span></span>

### <span data-ttu-id="06cde-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="06cde-111">-Account</span></span>
<span data-ttu-id="06cde-112">Das Data Lake Store-Konto zum Entfernen des vertrauenswürdigen Identitätsanbieters aus</span><span class="sxs-lookup"><span data-stu-id="06cde-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="06cde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06cde-113">-DefaultProfile</span></span>
<span data-ttu-id="06cde-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="06cde-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06cde-115">-Name</span><span class="sxs-lookup"><span data-stu-id="06cde-115">-Name</span></span>
<span data-ttu-id="06cde-116">Der Name des vertrauenswürdigen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="06cde-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="06cde-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06cde-117">-PassThru</span></span>
<span data-ttu-id="06cde-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="06cde-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06cde-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06cde-119">-ResourceGroupName</span></span>
<span data-ttu-id="06cde-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, aus dem der vertrauenswürdige Identitätsanbieter entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="06cde-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06cde-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06cde-121">-Confirm</span></span>
<span data-ttu-id="06cde-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06cde-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06cde-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06cde-123">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06cde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06cde-124">CommonParameters</span></span>
<span data-ttu-id="06cde-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06cde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06cde-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06cde-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06cde-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06cde-127">INPUTS</span></span>

### <span data-ttu-id="06cde-128">Keine</span><span class="sxs-lookup"><span data-stu-id="06cde-128">None</span></span>
<span data-ttu-id="06cde-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="06cde-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06cde-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06cde-130">OUTPUTS</span></span>

### <span data-ttu-id="06cde-131">bool</span><span class="sxs-lookup"><span data-stu-id="06cde-131">bool</span></span>
<span data-ttu-id="06cde-132">Wenn passthru angegeben ist, wird nach dem erfolgreichen Abschluss "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06cde-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="06cde-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="06cde-133">NOTES</span></span>

## <span data-ttu-id="06cde-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06cde-134">RELATED LINKS</span></span>

