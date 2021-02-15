---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: b6647ab3b729ab76d3cc02687bcd8dc342e788b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161921"
---
# <span data-ttu-id="57474-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="57474-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="57474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57474-102">SYNOPSIS</span></span>
<span data-ttu-id="57474-103">Fügt dem angegebenen Data Lake Store-Konto einen vertrauenswürdigen Identitätsanbieter hinzu.</span><span class="sxs-lookup"><span data-stu-id="57474-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="57474-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57474-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57474-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57474-105">DESCRIPTION</span></span>
<span data-ttu-id="57474-106">Das **Cmdlet "Add-AzDataLakeStoreTrustedIdProvider"** fügt dem angegebenen Data Lake Store-Konto einen vertrauenswürdigen Identitätsanbieter hinzu.</span><span class="sxs-lookup"><span data-stu-id="57474-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="57474-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57474-107">EXAMPLES</span></span>

### <span data-ttu-id="57474-108">Beispiel 1: Hinzufügen eines vertrauenswürdigen Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="57474-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="57474-109">Fügt den Anbieter "MyProvider" dem Konto "ContosoADL" mit dem Anbieterendpunkt " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 " hinzu.</span><span class="sxs-lookup"><span data-stu-id="57474-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="57474-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57474-110">PARAMETERS</span></span>

### <span data-ttu-id="57474-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="57474-111">-Account</span></span>
<span data-ttu-id="57474-112">Der Name des Data Lake Store-Kontos, dem der angegebene vertrauenswürdige Identitätsanbieter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="57474-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="57474-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57474-113">-DefaultProfile</span></span>
<span data-ttu-id="57474-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="57474-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57474-115">-Name</span><span class="sxs-lookup"><span data-stu-id="57474-115">-Name</span></span>
<span data-ttu-id="57474-116">Der Name des vertrauenswürdigen Identitätsanbieters, den Sie hinzufügen möchten</span><span class="sxs-lookup"><span data-stu-id="57474-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="57474-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="57474-117">-ProviderEndpoint</span></span>
<span data-ttu-id="57474-118">Der gültige Endpunkt des vertrauenswürdigen Anbieters im Format: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="57474-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="57474-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57474-119">-ResourceGroupName</span></span>
<span data-ttu-id="57474-120">Name der Ressourcengruppe, unter der der vertrauenswürdige Identitätsanbieter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="57474-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="57474-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57474-121">-Confirm</span></span>
<span data-ttu-id="57474-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57474-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57474-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="57474-123">-WhatIf</span></span>
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

### <span data-ttu-id="57474-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57474-124">CommonParameters</span></span>
<span data-ttu-id="57474-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57474-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57474-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57474-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57474-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57474-127">INPUTS</span></span>

### <span data-ttu-id="57474-128">System.String</span><span class="sxs-lookup"><span data-stu-id="57474-128">System.String</span></span>

## <span data-ttu-id="57474-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57474-129">OUTPUTS</span></span>

### <span data-ttu-id="57474-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="57474-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="57474-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="57474-131">NOTES</span></span>

## <span data-ttu-id="57474-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="57474-132">RELATED LINKS</span></span>
