---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: ed59b77a934787b1030166b24e9ed3af81698c16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936075"
---
# <span data-ttu-id="f8709-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f8709-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="f8709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8709-102">SYNOPSIS</span></span>
<span data-ttu-id="f8709-103">Deaktiviert die erweiterte Bedrohungsschutzrichtlinie für ein Speicher-/CosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="f8709-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="f8709-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8709-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8709-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8709-105">DESCRIPTION</span></span>
<span data-ttu-id="f8709-106">Das `Disable-AzSecurityAdvancedThreatProtection` Cmdlet deaktiviert die Bedrohungsschutzrichtlinie für ein Speicher-/CosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="f8709-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="f8709-107">Um dieses Cmdlet zu verwenden, geben Sie den *Parameter ResourceId* an.</span><span class="sxs-lookup"><span data-stu-id="f8709-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="f8709-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8709-108">EXAMPLES</span></span>

### <span data-ttu-id="f8709-109">Beispiel 1: Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="f8709-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="f8709-110">Mit diesem Befehl wird die erweiterte Bedrohungsschutzrichtlinie für die Ressourcen-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f8709-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="f8709-111">Beispiel 2: CosmosDB-Konto</span><span class="sxs-lookup"><span data-stu-id="f8709-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="f8709-112">Mit diesem Befehl wird die erweiterte Bedrohungsschutzrichtlinie für die Ressourcen-ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f8709-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="f8709-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f8709-113">PARAMETERS</span></span>

### <span data-ttu-id="f8709-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8709-114">-DefaultProfile</span></span>
<span data-ttu-id="f8709-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8709-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8709-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8709-116">-ResourceId</span></span>
<span data-ttu-id="f8709-117">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="f8709-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f8709-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8709-118">-Confirm</span></span>
<span data-ttu-id="f8709-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8709-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8709-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8709-120">-WhatIf</span></span>
<span data-ttu-id="f8709-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8709-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8709-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8709-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8709-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8709-123">CommonParameters</span></span>
<span data-ttu-id="f8709-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8709-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8709-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8709-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8709-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8709-126">INPUTS</span></span>

### <span data-ttu-id="f8709-127">Keine</span><span class="sxs-lookup"><span data-stu-id="f8709-127">None</span></span>

## <span data-ttu-id="f8709-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8709-128">OUTPUTS</span></span>

### <span data-ttu-id="f8709-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f8709-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="f8709-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f8709-130">NOTES</span></span>

## <span data-ttu-id="f8709-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f8709-131">RELATED LINKS</span></span>
