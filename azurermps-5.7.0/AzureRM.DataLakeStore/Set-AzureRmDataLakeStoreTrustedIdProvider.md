---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 29f9bbab5d3f7590d53bc405d80ea9e5c484fd5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497646"
---
# <span data-ttu-id="3cb7b-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="3cb7b-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="3cb7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cb7b-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb7b-103">Ändert den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3cb7b-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cb7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cb7b-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cb7b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cb7b-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb7b-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreTrustedIdProvider** " ändert den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3cb7b-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3cb7b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cb7b-107">EXAMPLES</span></span>

### <span data-ttu-id="3cb7b-108">Beispiel 1: Aktualisieren eines vertrauenswürdigen Identitätsanbieter Endpunkts</span><span class="sxs-lookup"><span data-stu-id="3cb7b-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="3cb7b-109">Dadurch wird die Anbieter-endpoing für die Firewall-Regel "MyProvider" im Konto "ContosoADL" auf "" aktualisiert. https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150</span><span class="sxs-lookup"><span data-stu-id="3cb7b-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="3cb7b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cb7b-110">PARAMETERS</span></span>

### <span data-ttu-id="3cb7b-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3cb7b-111">-Account</span></span>
<span data-ttu-id="3cb7b-112">Das Data Lake Store-Konto zum Hinzufügen des vertrauenswürdigen Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="3cb7b-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="3cb7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb7b-113">-DefaultProfile</span></span>
<span data-ttu-id="3cb7b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3cb7b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cb7b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3cb7b-115">-Name</span></span>
<span data-ttu-id="3cb7b-116">Der Name des vertrauenswürdigen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="3cb7b-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="3cb7b-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cb7b-117">-ProviderEndpoint</span></span>
<span data-ttu-id="3cb7b-118">Der gültige vertrauenswürdige Anbieterendpunkt im Format: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="3cb7b-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="3cb7b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb7b-119">-ResourceGroupName</span></span>
<span data-ttu-id="3cb7b-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das der vertrauenswürdige Identitätsanbieter aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cb7b-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="3cb7b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cb7b-121">-Confirm</span></span>
<span data-ttu-id="3cb7b-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cb7b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb7b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb7b-123">-WhatIf</span></span>
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

### <span data-ttu-id="3cb7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb7b-124">CommonParameters</span></span>
<span data-ttu-id="3cb7b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb7b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb7b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb7b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cb7b-127">INPUTS</span></span>

### <span data-ttu-id="3cb7b-128">Keine</span><span class="sxs-lookup"><span data-stu-id="3cb7b-128">None</span></span>
<span data-ttu-id="3cb7b-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3cb7b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3cb7b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cb7b-130">OUTPUTS</span></span>

### <span data-ttu-id="3cb7b-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="3cb7b-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="3cb7b-132">Der aktualisierte Trusted Identity-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="3cb7b-132">The updated trusted identity provider.</span></span>

## <span data-ttu-id="3cb7b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cb7b-133">NOTES</span></span>

## <span data-ttu-id="3cb7b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cb7b-134">RELATED LINKS</span></span>

