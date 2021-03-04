---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 10bda682881f35bc8401bec7304dcc1a68fd1d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936072"
---
# <span data-ttu-id="6ef1a-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6ef1a-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="6ef1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ef1a-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef1a-103">Aktiviert die erweiterte Bedrohungsschutzrichtlinie für ein Speicher-/CosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="6ef1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ef1a-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ef1a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ef1a-105">DESCRIPTION</span></span>
<span data-ttu-id="6ef1a-106">Das `Enable-AzSecurityAdvancedThreatProtection` Cmdlet aktiviert die Bedrohungsschutzrichtlinie für ein Speicher-/CosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="6ef1a-107">Um dieses Cmdlet zu verwenden, geben Sie den *Parameter ResourceId* an.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="6ef1a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ef1a-108">EXAMPLES</span></span>

### <span data-ttu-id="6ef1a-109">Beispiel 1: Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="6ef1a-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="6ef1a-110">Mit diesem Befehl wird die erweiterte Bedrohungsschutzrichtlinie für die Ressourcen-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="6ef1a-111">Beispiel 2: CosmosDB-Konto</span><span class="sxs-lookup"><span data-stu-id="6ef1a-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="6ef1a-112">Mit diesem Befehl wird die erweiterte Bedrohungsschutzrichtlinie für die Ressourcen-ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="6ef1a-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6ef1a-113">PARAMETERS</span></span>

### <span data-ttu-id="6ef1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef1a-114">-DefaultProfile</span></span>
<span data-ttu-id="6ef1a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ef1a-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ef1a-116">-ResourceId</span></span>
<span data-ttu-id="6ef1a-117">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef1a-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ef1a-118">-Confirm</span></span>
<span data-ttu-id="6ef1a-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ef1a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ef1a-120">-WhatIf</span></span>
<span data-ttu-id="6ef1a-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ef1a-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ef1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef1a-123">CommonParameters</span></span>
<span data-ttu-id="6ef1a-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ef1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef1a-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ef1a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef1a-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ef1a-126">INPUTS</span></span>

### <span data-ttu-id="6ef1a-127">Keine</span><span class="sxs-lookup"><span data-stu-id="6ef1a-127">None</span></span>

## <span data-ttu-id="6ef1a-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ef1a-128">OUTPUTS</span></span>

### <span data-ttu-id="6ef1a-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6ef1a-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="6ef1a-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6ef1a-130">NOTES</span></span>

## <span data-ttu-id="6ef1a-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6ef1a-131">RELATED LINKS</span></span>
