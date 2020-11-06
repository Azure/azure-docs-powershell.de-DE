---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/start-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
ms.openlocfilehash: 979db64fb11b4fffc901d96811b24be5c79f6b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497318"
---
# <span data-ttu-id="beaa6-101">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="beaa6-101">Start-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="beaa6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="beaa6-102">SYNOPSIS</span></span>
<span data-ttu-id="beaa6-103">Erstellt eine neue Migrations Konfiguration und startet die Migration von Entitäten von Standard-zu Premium-Namespaces</span><span class="sxs-lookup"><span data-stu-id="beaa6-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beaa6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="beaa6-104">SYNTAX</span></span>

```
Start-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="beaa6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="beaa6-105">DESCRIPTION</span></span>
<span data-ttu-id="beaa6-106">Das Cmdlet " **Start-AzureRmServiceBusMigration** " erstellt eine neue Migrations Konfiguration und startet die Migration von Entitäten von Standard-zu Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="beaa6-106">The **Start-AzureRmServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="beaa6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="beaa6-107">EXAMPLES</span></span>

### <span data-ttu-id="beaa6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="beaa6-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="beaa6-109">Erstellt eine neue Migrations Konfiguration für "TestingNamespaceStandardMirgation" in "TestingNamespacePremiumMirgation"-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="beaa6-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="beaa6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="beaa6-110">PARAMETERS</span></span>

### <span data-ttu-id="beaa6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="beaa6-111">-AsJob</span></span>
<span data-ttu-id="beaa6-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="beaa6-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaa6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beaa6-113">-DefaultProfile</span></span>
<span data-ttu-id="beaa6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="beaa6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaa6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="beaa6-115">-Name</span></span>
<span data-ttu-id="beaa6-116">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="beaa6-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaa6-117">-Postmigrations</span><span class="sxs-lookup"><span data-stu-id="beaa6-117">-PostMigrationName</span></span>
<span data-ttu-id="beaa6-118">Post-Migrations Name für Standrad-Namespace in Migration</span><span class="sxs-lookup"><span data-stu-id="beaa6-118">Post Migration Name for Standrad Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaa6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beaa6-119">-ResourceGroupName</span></span>
<span data-ttu-id="beaa6-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="beaa6-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaa6-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="beaa6-121">-TargetNameSpace</span></span>
<span data-ttu-id="beaa6-122">Premium-Namespace-Arm-ID</span><span class="sxs-lookup"><span data-stu-id="beaa6-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaa6-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="beaa6-123">-Confirm</span></span>
<span data-ttu-id="beaa6-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="beaa6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beaa6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beaa6-125">-WhatIf</span></span>
<span data-ttu-id="beaa6-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="beaa6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beaa6-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="beaa6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beaa6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaa6-128">CommonParameters</span></span>
<span data-ttu-id="beaa6-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beaa6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaa6-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beaa6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaa6-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="beaa6-131">INPUTS</span></span>

### <span data-ttu-id="beaa6-132">Keine</span><span class="sxs-lookup"><span data-stu-id="beaa6-132">None</span></span>

## <span data-ttu-id="beaa6-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="beaa6-133">OUTPUTS</span></span>

### <span data-ttu-id="beaa6-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="beaa6-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="beaa6-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="beaa6-135">NOTES</span></span>

## <span data-ttu-id="beaa6-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="beaa6-136">RELATED LINKS</span></span>
