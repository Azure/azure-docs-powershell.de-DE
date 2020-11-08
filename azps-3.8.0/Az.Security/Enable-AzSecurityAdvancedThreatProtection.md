---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 7e1bf5552d8c6fd6c7dff0c4478557059b0bc78a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996552"
---
# <span data-ttu-id="713e0-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="713e0-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="713e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="713e0-102">SYNOPSIS</span></span>
<span data-ttu-id="713e0-103">Aktiviert die erweiterte Bedrohungsschutz Richtlinie für ein Speicher-cosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="713e0-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="713e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="713e0-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="713e0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="713e0-105">DESCRIPTION</span></span>
<span data-ttu-id="713e0-106">Das `Enable-AzSecurityAdvancedThreatProtection` Cmdlet aktiviert die Bedrohungsschutz Richtlinie für ein Speicher-cosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="713e0-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="713e0-107">Um dieses Cmdlet zu verwenden, geben Sie den Parameter *resourcecode* an.</span><span class="sxs-lookup"><span data-stu-id="713e0-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="713e0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="713e0-108">EXAMPLES</span></span>

### <span data-ttu-id="713e0-109">Beispiel 1: Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="713e0-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="713e0-110">Mit diesem Befehl wird die erweiterte Bedrohungsschutz Richtlinie für die Ressourcen-ID aktiviert `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="713e0-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="713e0-111">Beispiel 2: CosmosDB-Konto</span><span class="sxs-lookup"><span data-stu-id="713e0-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="713e0-112">Mit diesem Befehl wird die erweiterte Bedrohungsschutz Richtlinie für die Ressourcen-ID aktiviert ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="713e0-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="713e0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="713e0-113">PARAMETERS</span></span>

### <span data-ttu-id="713e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="713e0-114">-DefaultProfile</span></span>
<span data-ttu-id="713e0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="713e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="713e0-116">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="713e0-116">-ResourceId</span></span>
<span data-ttu-id="713e0-117">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="713e0-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="713e0-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="713e0-118">-Confirm</span></span>
<span data-ttu-id="713e0-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="713e0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="713e0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="713e0-120">-WhatIf</span></span>
<span data-ttu-id="713e0-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="713e0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="713e0-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="713e0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="713e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="713e0-123">CommonParameters</span></span>
<span data-ttu-id="713e0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="713e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="713e0-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="713e0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="713e0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="713e0-126">INPUTS</span></span>

### <span data-ttu-id="713e0-127">Keine</span><span class="sxs-lookup"><span data-stu-id="713e0-127">None</span></span>

## <span data-ttu-id="713e0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="713e0-128">OUTPUTS</span></span>

### <span data-ttu-id="713e0-129">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="713e0-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="713e0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="713e0-130">NOTES</span></span>

## <span data-ttu-id="713e0-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="713e0-131">RELATED LINKS</span></span>
