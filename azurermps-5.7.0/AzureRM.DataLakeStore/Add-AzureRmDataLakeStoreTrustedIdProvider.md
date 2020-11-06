---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 302ad6ac14ad9fcb08053e70afb7951e72c6e027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496598"
---
# <span data-ttu-id="208a1-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="208a1-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="208a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="208a1-102">SYNOPSIS</span></span>
<span data-ttu-id="208a1-103">Fügt einen vertrauenswürdigen Identitätsanbieter zum angegebenen Data Lake Store-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="208a1-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="208a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="208a1-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="208a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="208a1-105">DESCRIPTION</span></span>
<span data-ttu-id="208a1-106">Mit dem Cmdlet **Add-AzureRmDataLakeStoreTrustedIdProvider** wird ein vertrauenswürdiger Identitätsanbieter zum angegebenen Data Lake Store-Konto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="208a1-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="208a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="208a1-107">EXAMPLES</span></span>

### <span data-ttu-id="208a1-108">Beispiel 1: Hinzufügen eines vertrauenswürdigen Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="208a1-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="208a1-109">Fügt den Anbieter "MyProvider" zu Konto "ContosoADL" mit dem Anbieterendpunkt "" hinzu. https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150</span><span class="sxs-lookup"><span data-stu-id="208a1-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="208a1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="208a1-110">PARAMETERS</span></span>

### <span data-ttu-id="208a1-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="208a1-111">-Account</span></span>
<span data-ttu-id="208a1-112">Der Name des Daten Lake Store-Kontos, dem der angegebene vertrauenswürdige Identitätsanbieter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="208a1-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="208a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208a1-113">-DefaultProfile</span></span>
<span data-ttu-id="208a1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="208a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="208a1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="208a1-115">-Name</span></span>
<span data-ttu-id="208a1-116">Der Name des hinzuzufügenden vertrauenswürdigen Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="208a1-116">The name of the trusted identity provider to add</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="208a1-117">-ProviderEndpoint</span></span>
<span data-ttu-id="208a1-118">Der gültige vertrauenswürdige Anbieterendpunkt im Format: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="208a1-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="208a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="208a1-120">Der Name der Ressourcengruppe, unter der sich das Konto befindet, dem der vertrauenswürdige Identitätsanbieter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="208a1-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="208a1-121">-Confirm</span></span>
<span data-ttu-id="208a1-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="208a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="208a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208a1-123">-WhatIf</span></span>
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

### <span data-ttu-id="208a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208a1-124">CommonParameters</span></span>
<span data-ttu-id="208a1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="208a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208a1-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="208a1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208a1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="208a1-127">INPUTS</span></span>

### <span data-ttu-id="208a1-128">Keine</span><span class="sxs-lookup"><span data-stu-id="208a1-128">None</span></span>
<span data-ttu-id="208a1-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="208a1-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="208a1-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="208a1-130">OUTPUTS</span></span>

### <span data-ttu-id="208a1-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="208a1-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="208a1-132">Der hinzugefügte vertrauenswürdige Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="208a1-132">The added Trusted Identity Provider.</span></span>

## <span data-ttu-id="208a1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="208a1-133">NOTES</span></span>

## <span data-ttu-id="208a1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="208a1-134">RELATED LINKS</span></span>

