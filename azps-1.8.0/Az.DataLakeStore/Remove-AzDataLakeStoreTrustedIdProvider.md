---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: a93eb93a02c0ba1f5654258da0405f723e69873d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661261"
---
# <span data-ttu-id="cb371-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="cb371-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="cb371-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb371-102">SYNOPSIS</span></span>
<span data-ttu-id="cb371-103">Entfernt den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb371-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="cb371-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb371-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb371-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb371-105">DESCRIPTION</span></span>
<span data-ttu-id="cb371-106">Mit dem Cmdlet **Remove-AzDataLakeStoreTrustedIdProvider** wird der angegebene Trusted Identity-Anbieter im angegebenen Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="cb371-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="cb371-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb371-107">EXAMPLES</span></span>

### <span data-ttu-id="cb371-108">Beispiel 1: Entfernen Sie einen vertrauenswürdigen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="cb371-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="cb371-109">Entfernt den Anbieter "MyProvider" aus dem Konto "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="cb371-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="cb371-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb371-110">PARAMETERS</span></span>

### <span data-ttu-id="cb371-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="cb371-111">-Account</span></span>
<span data-ttu-id="cb371-112">Das Data Lake Store-Konto zum Entfernen des vertrauenswürdigen Identitätsanbieters aus</span><span class="sxs-lookup"><span data-stu-id="cb371-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="cb371-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb371-113">-DefaultProfile</span></span>
<span data-ttu-id="cb371-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cb371-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb371-115">-Name</span><span class="sxs-lookup"><span data-stu-id="cb371-115">-Name</span></span>
<span data-ttu-id="cb371-116">Der Name des vertrauenswürdigen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="cb371-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="cb371-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb371-117">-PassThru</span></span>
<span data-ttu-id="cb371-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="cb371-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb371-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb371-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb371-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, aus dem der vertrauenswürdige Identitätsanbieter entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb371-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb371-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cb371-121">-Confirm</span></span>
<span data-ttu-id="cb371-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb371-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb371-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb371-123">-WhatIf</span></span>
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

### <span data-ttu-id="cb371-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb371-124">CommonParameters</span></span>
<span data-ttu-id="cb371-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb371-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb371-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb371-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb371-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb371-127">INPUTS</span></span>

### <span data-ttu-id="cb371-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cb371-128">System.String</span></span>

### <span data-ttu-id="cb371-129">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="cb371-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cb371-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb371-130">OUTPUTS</span></span>

### <span data-ttu-id="cb371-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb371-131">System.Boolean</span></span>

## <span data-ttu-id="cb371-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb371-132">NOTES</span></span>

## <span data-ttu-id="cb371-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb371-133">RELATED LINKS</span></span>
