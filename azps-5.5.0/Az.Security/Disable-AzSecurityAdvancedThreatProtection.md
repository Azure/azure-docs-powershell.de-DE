---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e7195131830fd5b19a6d67b4fae5583374da7d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145884"
---
# <span data-ttu-id="41fc0-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="41fc0-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="41fc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="41fc0-103">Deaktiviert die erweiterte Threat Protection-Richtlinie für ein Speicher-/DatensDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="41fc0-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="41fc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41fc0-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41fc0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="41fc0-106">Das `Disable-AzSecurityAdvancedThreatProtection` Cmdlet deaktiviert die Threat Protection Policy für ein Speicher-/MediensDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="41fc0-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="41fc0-107">Um dieses Cmdlet zu verwenden, geben Sie den *Parameter "ResourceId"* an.</span><span class="sxs-lookup"><span data-stu-id="41fc0-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="41fc0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="41fc0-108">EXAMPLES</span></span>

### <span data-ttu-id="41fc0-109">Beispiel 1: Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="41fc0-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="41fc0-110">Mit diesem Befehl wird die erweiterte Threat Protection-Richtlinie für die Ressourcen-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="41fc0-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="41fc0-111">Beispiel 2: Abt.</span><span class="sxs-lookup"><span data-stu-id="41fc0-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="41fc0-112">Mit diesem Befehl wird die erweiterte Threat Protection-Richtlinie für die Ressourcen-ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="41fc0-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="41fc0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41fc0-113">PARAMETERS</span></span>

### <span data-ttu-id="41fc0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fc0-114">-DefaultProfile</span></span>
<span data-ttu-id="41fc0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41fc0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41fc0-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41fc0-116">-ResourceId</span></span>
<span data-ttu-id="41fc0-117">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="41fc0-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="41fc0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41fc0-118">-Confirm</span></span>
<span data-ttu-id="41fc0-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41fc0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41fc0-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="41fc0-120">-WhatIf</span></span>
<span data-ttu-id="41fc0-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41fc0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41fc0-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41fc0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41fc0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fc0-123">CommonParameters</span></span>
<span data-ttu-id="41fc0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41fc0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fc0-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41fc0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fc0-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="41fc0-126">INPUTS</span></span>

### <span data-ttu-id="41fc0-127">Keine</span><span class="sxs-lookup"><span data-stu-id="41fc0-127">None</span></span>

## <span data-ttu-id="41fc0-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="41fc0-128">OUTPUTS</span></span>

### <span data-ttu-id="41fc0-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="41fc0-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="41fc0-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="41fc0-130">NOTES</span></span>

## <span data-ttu-id="41fc0-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="41fc0-131">RELATED LINKS</span></span>
