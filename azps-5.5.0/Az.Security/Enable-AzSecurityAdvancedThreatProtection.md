---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 3db63fad33fe49fe7aa001f13759e41e7cd7c856
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145849"
---
# <span data-ttu-id="93eeb-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="93eeb-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="93eeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="93eeb-103">Aktiviert die erweiterte Threat Protection-Richtlinie für ein Speicher-/DatensDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="93eeb-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="93eeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93eeb-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93eeb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="93eeb-106">Das `Enable-AzSecurityAdvancedThreatProtection` Cmdlet aktiviert die Threat Protection Policy für ein Speicher-/DatensDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="93eeb-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="93eeb-107">Um dieses Cmdlet zu verwenden, geben Sie den *Parameter "ResourceId"* an.</span><span class="sxs-lookup"><span data-stu-id="93eeb-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="93eeb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93eeb-108">EXAMPLES</span></span>

### <span data-ttu-id="93eeb-109">Beispiel 1: Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="93eeb-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="93eeb-110">Dieser Befehl aktiviert die erweiterte Threat Protection-Richtlinie für die `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="93eeb-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="93eeb-111">Beispiel 2: Abt.</span><span class="sxs-lookup"><span data-stu-id="93eeb-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="93eeb-112">Dieser Befehl aktiviert die erweiterte Threat Protection-Richtlinie für die ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="93eeb-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="93eeb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93eeb-113">PARAMETERS</span></span>

### <span data-ttu-id="93eeb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93eeb-114">-DefaultProfile</span></span>
<span data-ttu-id="93eeb-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93eeb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93eeb-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93eeb-116">-ResourceId</span></span>
<span data-ttu-id="93eeb-117">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="93eeb-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="93eeb-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93eeb-118">-Confirm</span></span>
<span data-ttu-id="93eeb-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93eeb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93eeb-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="93eeb-120">-WhatIf</span></span>
<span data-ttu-id="93eeb-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93eeb-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93eeb-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93eeb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93eeb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93eeb-123">CommonParameters</span></span>
<span data-ttu-id="93eeb-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93eeb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93eeb-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93eeb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93eeb-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93eeb-126">INPUTS</span></span>

### <span data-ttu-id="93eeb-127">Keine</span><span class="sxs-lookup"><span data-stu-id="93eeb-127">None</span></span>

## <span data-ttu-id="93eeb-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93eeb-128">OUTPUTS</span></span>

### <span data-ttu-id="93eeb-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="93eeb-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="93eeb-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="93eeb-130">NOTES</span></span>

## <span data-ttu-id="93eeb-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="93eeb-131">RELATED LINKS</span></span>
