---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: deef0be93c3a80c0db9762907eb52cdc51da9ed3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659469"
---
# <span data-ttu-id="9a141-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="9a141-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="9a141-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a141-102">SYNOPSIS</span></span>
<span data-ttu-id="9a141-103">Aktiviert die erweiterte Bedrohungsschutz Richtlinie für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="9a141-103">Enables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="9a141-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a141-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a141-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a141-105">DESCRIPTION</span></span>
<span data-ttu-id="9a141-106">Das `Enable-AzSecurityAdvancedThreatProtection` Cmdlet aktiviert die Threat protetion-Richtlinie für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="9a141-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="9a141-107">Um dieses Cmdlet zu verwenden, geben Sie den Parameter *resourcecode* an.</span><span class="sxs-lookup"><span data-stu-id="9a141-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="9a141-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a141-108">EXAMPLES</span></span>

### <span data-ttu-id="9a141-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a141-109">Example 1</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="9a141-110">Mit diesem Befehl wird die erweiterte Bedrohungsschutz Richtlinie für die Ressourcen-ID aktiviert `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="9a141-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="9a141-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a141-111">PARAMETERS</span></span>

### <span data-ttu-id="9a141-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a141-112">-DefaultProfile</span></span>
<span data-ttu-id="9a141-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a141-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a141-114">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9a141-114">-ResourceId</span></span>
<span data-ttu-id="9a141-115">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9a141-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9a141-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a141-116">-Confirm</span></span>
<span data-ttu-id="9a141-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a141-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a141-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a141-118">-WhatIf</span></span>
<span data-ttu-id="9a141-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a141-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a141-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a141-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a141-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a141-121">CommonParameters</span></span>
<span data-ttu-id="9a141-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a141-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a141-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a141-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a141-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a141-124">INPUTS</span></span>

### <span data-ttu-id="9a141-125">Keine</span><span class="sxs-lookup"><span data-stu-id="9a141-125">None</span></span>

## <span data-ttu-id="9a141-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a141-126">OUTPUTS</span></span>

### <span data-ttu-id="9a141-127">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="9a141-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="9a141-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a141-128">NOTES</span></span>

## <span data-ttu-id="9a141-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a141-129">RELATED LINKS</span></span>
