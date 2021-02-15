---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174033"
---
# <span data-ttu-id="e29ed-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="e29ed-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="e29ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e29ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e29ed-103">Erstellt eine neue Migrationskonfiguration und beginnt mit der Migration von Entitäten aus Standard- zu Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="e29ed-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="e29ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e29ed-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e29ed-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e29ed-105">DESCRIPTION</span></span>
<span data-ttu-id="e29ed-106">Das **Cmdlet "Start-AzServiceBusMigration"** erstellt eine neue Migrationskonfiguration und beginnt mit der Migration von Entitäten aus Standard- zu Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="e29ed-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="e29ed-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e29ed-107">EXAMPLES</span></span>

### <span data-ttu-id="e29ed-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e29ed-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="e29ed-109">Erstellt eine neue Migrationskonfiguration für 'TestingNamespaceStandardMigration' in 'TestingNamespacePremiumMigration'-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="e29ed-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="e29ed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e29ed-110">PARAMETERS</span></span>

### <span data-ttu-id="e29ed-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e29ed-111">-AsJob</span></span>
<span data-ttu-id="e29ed-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e29ed-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e29ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29ed-113">-DefaultProfile</span></span>
<span data-ttu-id="e29ed-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e29ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e29ed-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e29ed-115">-Name</span></span>
<span data-ttu-id="e29ed-116">Standardnamespacename</span><span class="sxs-lookup"><span data-stu-id="e29ed-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="e29ed-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="e29ed-117">-PostMigrationName</span></span>
<span data-ttu-id="e29ed-118">Name nach der Migration für Standardnamespace in der Migration</span><span class="sxs-lookup"><span data-stu-id="e29ed-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="e29ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="e29ed-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e29ed-120">Resource Group Name</span></span>

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

### <span data-ttu-id="e29ed-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="e29ed-121">-TargetNameSpace</span></span>
<span data-ttu-id="e29ed-122">Premium-Namespace ARM-ID</span><span class="sxs-lookup"><span data-stu-id="e29ed-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="e29ed-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e29ed-123">-Confirm</span></span>
<span data-ttu-id="e29ed-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e29ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e29ed-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e29ed-125">-WhatIf</span></span>
<span data-ttu-id="e29ed-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e29ed-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e29ed-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e29ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e29ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29ed-128">CommonParameters</span></span>
<span data-ttu-id="e29ed-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29ed-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e29ed-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29ed-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e29ed-131">INPUTS</span></span>

### <span data-ttu-id="e29ed-132">Keine</span><span class="sxs-lookup"><span data-stu-id="e29ed-132">None</span></span>

## <span data-ttu-id="e29ed-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e29ed-133">OUTPUTS</span></span>

### <span data-ttu-id="e29ed-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e29ed-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="e29ed-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e29ed-135">NOTES</span></span>

## <span data-ttu-id="e29ed-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e29ed-136">RELATED LINKS</span></span>
