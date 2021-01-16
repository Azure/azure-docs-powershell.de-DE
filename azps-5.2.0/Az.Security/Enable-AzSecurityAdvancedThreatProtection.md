---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 3db63fad33fe49fe7aa001f13759e41e7cd7c856
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296512"
---
# <span data-ttu-id="97bd5-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="97bd5-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="97bd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="97bd5-103">Aktiviert die erweiterte Threat Protection-Richtlinie für ein Speicher-/DatensDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="97bd5-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="97bd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97bd5-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97bd5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="97bd5-106">Das `Enable-AzSecurityAdvancedThreatProtection` Cmdlet aktiviert die Threat Protection Policy für ein Speicher-/DatensDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="97bd5-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="97bd5-107">Um dieses Cmdlet zu verwenden, geben Sie den *Parameter "ResourceId"* an.</span><span class="sxs-lookup"><span data-stu-id="97bd5-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="97bd5-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97bd5-108">EXAMPLES</span></span>

### <span data-ttu-id="97bd5-109">Beispiel 1: Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="97bd5-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="97bd5-110">Dieser Befehl aktiviert die erweiterte Threat Protection-Richtlinie für die `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="97bd5-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="97bd5-111">Beispiel 2: Abt.</span><span class="sxs-lookup"><span data-stu-id="97bd5-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="97bd5-112">Dieser Befehl aktiviert die erweiterte Threat Protection-Richtlinie für die ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="97bd5-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="97bd5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97bd5-113">PARAMETERS</span></span>

### <span data-ttu-id="97bd5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97bd5-114">-DefaultProfile</span></span>
<span data-ttu-id="97bd5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97bd5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97bd5-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97bd5-116">-ResourceId</span></span>
<span data-ttu-id="97bd5-117">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="97bd5-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="97bd5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97bd5-118">-Confirm</span></span>
<span data-ttu-id="97bd5-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="97bd5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97bd5-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="97bd5-120">-WhatIf</span></span>
<span data-ttu-id="97bd5-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97bd5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97bd5-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97bd5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97bd5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97bd5-123">CommonParameters</span></span>
<span data-ttu-id="97bd5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97bd5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97bd5-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97bd5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97bd5-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97bd5-126">INPUTS</span></span>

### <span data-ttu-id="97bd5-127">Keine</span><span class="sxs-lookup"><span data-stu-id="97bd5-127">None</span></span>

## <span data-ttu-id="97bd5-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97bd5-128">OUTPUTS</span></span>

### <span data-ttu-id="97bd5-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="97bd5-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="97bd5-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97bd5-130">NOTES</span></span>

## <span data-ttu-id="97bd5-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97bd5-131">RELATED LINKS</span></span>
