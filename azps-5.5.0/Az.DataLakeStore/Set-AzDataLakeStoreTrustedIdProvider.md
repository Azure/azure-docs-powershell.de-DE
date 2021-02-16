---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c4de7a926e4095ad8bb45a25647305617988330d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144313"
---
# <span data-ttu-id="b3937-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b3937-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="b3937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3937-102">SYNOPSIS</span></span>
<span data-ttu-id="b3937-103">Ändert den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b3937-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b3937-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3937-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3937-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3937-105">DESCRIPTION</span></span>
<span data-ttu-id="b3937-106">Das **Cmdlet "Set-AzDataLakeStoreTrustedIdProvider"** ändert den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b3937-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b3937-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3937-107">EXAMPLES</span></span>

### <span data-ttu-id="b3937-108">Beispiel 1: Aktualisieren eines Endpunkts eines vertrauenswürdigen Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="b3937-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="b3937-109">Dadurch wird der Anbieterendpunkt für die Firewallregel "MyProvider" im Konto "ContosoADL" auf " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 " aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b3937-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="b3937-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3937-110">PARAMETERS</span></span>

### <span data-ttu-id="b3937-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="b3937-111">-Account</span></span>
<span data-ttu-id="b3937-112">Das Data Lake Store-Konto, dem der vertrauenswürdige Identitätsanbieter hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="b3937-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="b3937-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3937-113">-DefaultProfile</span></span>
<span data-ttu-id="b3937-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b3937-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3937-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b3937-115">-Name</span></span>
<span data-ttu-id="b3937-116">Der Name des vertrauenswürdigen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="b3937-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="b3937-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3937-117">-ProviderEndpoint</span></span>
<span data-ttu-id="b3937-118">Der gültige Endpunkt des vertrauenswürdigen Anbieters im Format: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="b3937-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="b3937-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3937-119">-ResourceGroupName</span></span>
<span data-ttu-id="b3937-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das der vertrauenswürdige Identitätsanbieter aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3937-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="b3937-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3937-121">-Confirm</span></span>
<span data-ttu-id="b3937-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3937-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3937-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b3937-123">-WhatIf</span></span>
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

### <span data-ttu-id="b3937-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3937-124">CommonParameters</span></span>
<span data-ttu-id="b3937-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3937-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3937-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3937-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3937-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3937-127">INPUTS</span></span>

### <span data-ttu-id="b3937-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b3937-128">System.String</span></span>

## <span data-ttu-id="b3937-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3937-129">OUTPUTS</span></span>

### <span data-ttu-id="b3937-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b3937-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="b3937-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3937-131">NOTES</span></span>

## <span data-ttu-id="b3937-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3937-132">RELATED LINKS</span></span>
