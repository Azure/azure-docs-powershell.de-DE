---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 66d8f15c58d1b4b92f19e23f5940ed7c8ba45d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659340"
---
# <span data-ttu-id="3cf6b-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3cf6b-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="3cf6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cf6b-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf6b-103">Erstellt eine neue Migrations Konfiguration und startet die Migration von Entitäten von Standard-zu Premium-Namespaces</span><span class="sxs-lookup"><span data-stu-id="3cf6b-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="3cf6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cf6b-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cf6b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cf6b-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf6b-106">Das Cmdlet " **Start-AzServiceBusMigration** " erstellt eine neue Migrations Konfiguration und startet die Migration von Entitäten von Standard-zu Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3cf6b-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="3cf6b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cf6b-107">EXAMPLES</span></span>

### <span data-ttu-id="3cf6b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3cf6b-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="3cf6b-109">Erstellt eine neue Migrations Konfiguration für "TestingNamespaceStandardMirgation" in "TestingNamespacePremiumMirgation"-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3cf6b-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="3cf6b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cf6b-110">PARAMETERS</span></span>

### <span data-ttu-id="3cf6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cf6b-111">-AsJob</span></span>
<span data-ttu-id="3cf6b-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3cf6b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cf6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf6b-113">-DefaultProfile</span></span>
<span data-ttu-id="3cf6b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cf6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf6b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3cf6b-115">-Name</span></span>
<span data-ttu-id="3cf6b-116">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3cf6b-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="3cf6b-117">-Postmigrations</span><span class="sxs-lookup"><span data-stu-id="3cf6b-117">-PostMigrationName</span></span>
<span data-ttu-id="3cf6b-118">Post-Migrations Name für Standrad-Namespace in Migration</span><span class="sxs-lookup"><span data-stu-id="3cf6b-118">Post Migration Name for Standrad Namespace in Migration</span></span>

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

### <span data-ttu-id="3cf6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="3cf6b-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3cf6b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="3cf6b-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="3cf6b-121">-TargetNameSpace</span></span>
<span data-ttu-id="3cf6b-122">Premium-Namespace-Arm-ID</span><span class="sxs-lookup"><span data-stu-id="3cf6b-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="3cf6b-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cf6b-123">-Confirm</span></span>
<span data-ttu-id="3cf6b-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cf6b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf6b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf6b-125">-WhatIf</span></span>
<span data-ttu-id="3cf6b-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cf6b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf6b-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cf6b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf6b-128">CommonParameters</span></span>
<span data-ttu-id="3cf6b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf6b-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf6b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf6b-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cf6b-131">INPUTS</span></span>

### <span data-ttu-id="3cf6b-132">Keine</span><span class="sxs-lookup"><span data-stu-id="3cf6b-132">None</span></span>

## <span data-ttu-id="3cf6b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cf6b-133">OUTPUTS</span></span>

### <span data-ttu-id="3cf6b-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3cf6b-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="3cf6b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cf6b-135">NOTES</span></span>

## <span data-ttu-id="3cf6b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cf6b-136">RELATED LINKS</span></span>
