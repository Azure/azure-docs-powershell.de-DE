---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: c2d2bcaf95b7eda010cc299a7c20cfd703f7eadb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823344"
---
# <span data-ttu-id="c2863-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c2863-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="c2863-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2863-102">SYNOPSIS</span></span>
<span data-ttu-id="c2863-103">Deaktiviert die erweiterte Bedrohungsschutz Richtlinie für ein Speicher-cosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="c2863-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="c2863-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2863-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2863-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2863-105">DESCRIPTION</span></span>
<span data-ttu-id="c2863-106">Das `Disable-AzSecurityAdvancedThreatProtection` Cmdlet deaktiviert die Richtlinie für den Bedrohungsschutz für ein Speicher-cosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="c2863-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="c2863-107">Um dieses Cmdlet zu verwenden, geben Sie den Parameter *resourcecode* an.</span><span class="sxs-lookup"><span data-stu-id="c2863-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="c2863-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2863-108">EXAMPLES</span></span>

### <span data-ttu-id="c2863-109">Beispiel 1: Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="c2863-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="c2863-110">Dieser Befehl deaktiviert die erweiterte Bedrohungsschutz Richtlinie für die Ressourcen-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="c2863-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="c2863-111">Beispiel 2: CosmosDB-Konto</span><span class="sxs-lookup"><span data-stu-id="c2863-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="c2863-112">Dieser Befehl deaktiviert die erweiterte Bedrohungsschutz Richtlinie für die Ressourcen-ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="c2863-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="c2863-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2863-113">PARAMETERS</span></span>

### <span data-ttu-id="c2863-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2863-114">-DefaultProfile</span></span>
<span data-ttu-id="c2863-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2863-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2863-116">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c2863-116">-ResourceId</span></span>
<span data-ttu-id="c2863-117">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c2863-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c2863-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2863-118">-Confirm</span></span>
<span data-ttu-id="c2863-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2863-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2863-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2863-120">-WhatIf</span></span>
<span data-ttu-id="c2863-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2863-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2863-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2863-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2863-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2863-123">CommonParameters</span></span>
<span data-ttu-id="c2863-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2863-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2863-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2863-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2863-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2863-126">INPUTS</span></span>

### <span data-ttu-id="c2863-127">Keine</span><span class="sxs-lookup"><span data-stu-id="c2863-127">None</span></span>

## <span data-ttu-id="c2863-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2863-128">OUTPUTS</span></span>

### <span data-ttu-id="c2863-129">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c2863-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="c2863-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2863-130">NOTES</span></span>

## <span data-ttu-id="c2863-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2863-131">RELATED LINKS</span></span>
