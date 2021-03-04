---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d8762d0ddd689d40397bee423e8166aa8dd7a6a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923776"
---
# <span data-ttu-id="3f9ed-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="3f9ed-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="3f9ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f9ed-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9ed-103">Entfernt den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f9ed-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3f9ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f9ed-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f9ed-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f9ed-105">DESCRIPTION</span></span>
<span data-ttu-id="3f9ed-106">Das **Cmdlet Remove-AzDataLakeStoreTrustedIdProvider** entfernt den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f9ed-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3f9ed-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f9ed-107">EXAMPLES</span></span>

### <span data-ttu-id="3f9ed-108">Beispiel 1: Entfernen eines vertrauenswürdigen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="3f9ed-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="3f9ed-109">Entfernt den Anbieter "MyProvider" aus dem Konto "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="3f9ed-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="3f9ed-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3f9ed-110">PARAMETERS</span></span>

### <span data-ttu-id="3f9ed-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3f9ed-111">-Account</span></span>
<span data-ttu-id="3f9ed-112">Das Data Lake Store-Konto zum Entfernen des vertrauenswürdigen Identitätsanbieters aus</span><span class="sxs-lookup"><span data-stu-id="3f9ed-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="3f9ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9ed-113">-DefaultProfile</span></span>
<span data-ttu-id="3f9ed-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3f9ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f9ed-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3f9ed-115">-Name</span></span>
<span data-ttu-id="3f9ed-116">Der Name des vertrauenswürdigen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="3f9ed-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="3f9ed-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f9ed-117">-PassThru</span></span>
<span data-ttu-id="3f9ed-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="3f9ed-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="3f9ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f9ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="3f9ed-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, aus dem der vertrauenswürdige Identitätsanbieter entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f9ed-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="3f9ed-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f9ed-121">-Confirm</span></span>
<span data-ttu-id="3f9ed-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f9ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f9ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f9ed-123">-WhatIf</span></span>
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

### <span data-ttu-id="3f9ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9ed-124">CommonParameters</span></span>
<span data-ttu-id="3f9ed-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f9ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9ed-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f9ed-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9ed-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f9ed-127">INPUTS</span></span>

### <span data-ttu-id="3f9ed-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3f9ed-128">System.String</span></span>

### <span data-ttu-id="3f9ed-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3f9ed-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3f9ed-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f9ed-130">OUTPUTS</span></span>

### <span data-ttu-id="3f9ed-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f9ed-131">System.Boolean</span></span>

## <span data-ttu-id="3f9ed-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3f9ed-132">NOTES</span></span>

## <span data-ttu-id="3f9ed-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3f9ed-133">RELATED LINKS</span></span>
