---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 12e84ee5456acc0c56eed0f35b0bf3c23813b31f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479246"
---
# <span data-ttu-id="819a3-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="819a3-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="819a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="819a3-102">SYNOPSIS</span></span>
<span data-ttu-id="819a3-103">Ändert den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="819a3-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="819a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="819a3-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="819a3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="819a3-105">DESCRIPTION</span></span>
<span data-ttu-id="819a3-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreTrustedIdProvider** " ändert den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="819a3-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="819a3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="819a3-107">EXAMPLES</span></span>

### <span data-ttu-id="819a3-108">Beispiel 1: Aktualisieren eines vertrauenswürdigen Identitätsanbieter Endpunkts</span><span class="sxs-lookup"><span data-stu-id="819a3-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="819a3-109">Dadurch wird die Anbieter-endpoing für die Firewall-Regel "MyProvider" im Konto "ContosoADL" auf "" aktualisiert. https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150</span><span class="sxs-lookup"><span data-stu-id="819a3-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="819a3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="819a3-110">PARAMETERS</span></span>

### <span data-ttu-id="819a3-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="819a3-111">-Account</span></span>
<span data-ttu-id="819a3-112">Das Data Lake Store-Konto zum Hinzufügen des vertrauenswürdigen Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="819a3-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="819a3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="819a3-113">-Name</span></span>
<span data-ttu-id="819a3-114">Der Name des vertrauenswürdigen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="819a3-114">The name of the trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819a3-115">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="819a3-115">-ProviderEndpoint</span></span>
<span data-ttu-id="819a3-116">Der gültige vertrauenswürdige Anbieterendpunkt im Format: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="819a3-116">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="819a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="819a3-118">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das der vertrauenswürdige Identitätsanbieter aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="819a3-118">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819a3-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="819a3-119">-Confirm</span></span>
<span data-ttu-id="819a3-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="819a3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819a3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="819a3-121">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819a3-122">-DefaultProfile</span></span>
<span data-ttu-id="819a3-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="819a3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="819a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819a3-124">CommonParameters</span></span>
<span data-ttu-id="819a3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819a3-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819a3-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="819a3-127">INPUTS</span></span>

## <span data-ttu-id="819a3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="819a3-128">OUTPUTS</span></span>

### <span data-ttu-id="819a3-129">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="819a3-129">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="819a3-130">Der aktualisierte Trusted Identity-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="819a3-130">The updated trusted identity provider.</span></span>

## <span data-ttu-id="819a3-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="819a3-131">NOTES</span></span>

## <span data-ttu-id="819a3-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="819a3-132">RELATED LINKS</span></span>

