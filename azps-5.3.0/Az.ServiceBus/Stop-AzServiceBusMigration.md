---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471844"
---
# <span data-ttu-id="a557c-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a557c-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="a557c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a557c-102">SYNOPSIS</span></span>
<span data-ttu-id="a557c-103">{{Fill in the Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="a557c-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="a557c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a557c-104">SYNTAX</span></span>

### <span data-ttu-id="a557c-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a557c-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a557c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a557c-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a557c-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a557c-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a557c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a557c-108">DESCRIPTION</span></span>
<span data-ttu-id="a557c-109">Mit **den "Stop-AzServiceBusMigration"-Cmdlets** wird die Migration zwischen dem Standard- und dem Premiumnamespace beendet.</span><span class="sxs-lookup"><span data-stu-id="a557c-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="a557c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a557c-110">EXAMPLES</span></span>

### <span data-ttu-id="a557c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a557c-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="a557c-112">Das Cmdlet beendet die Migration zwischen standard-Namespace und Premium-Namespace, die beim Erstellen der Migrationskonfiguration bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a557c-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="a557c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a557c-113">PARAMETERS</span></span>

### <span data-ttu-id="a557c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a557c-114">-DefaultProfile</span></span>
<span data-ttu-id="a557c-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a557c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a557c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a557c-116">-InputObject</span></span>
<span data-ttu-id="a557c-117">Service Bus Migration Configuration Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="a557c-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a557c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a557c-118">-Name</span></span>
<span data-ttu-id="a557c-119">Standardnamespacename</span><span class="sxs-lookup"><span data-stu-id="a557c-119">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a557c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a557c-120">-PassThru</span></span>
<span data-ttu-id="a557c-121">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a557c-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a557c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a557c-122">-ResourceGroupName</span></span>
<span data-ttu-id="a557c-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a557c-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a557c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a557c-124">-ResourceId</span></span>
<span data-ttu-id="a557c-125">Service Bus Migration Configuration Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="a557c-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a557c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a557c-126">-Confirm</span></span>
<span data-ttu-id="a557c-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a557c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a557c-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a557c-128">-WhatIf</span></span>
<span data-ttu-id="a557c-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a557c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a557c-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a557c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a557c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a557c-131">CommonParameters</span></span>
<span data-ttu-id="a557c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a557c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a557c-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a557c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a557c-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a557c-134">INPUTS</span></span>

### <span data-ttu-id="a557c-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a557c-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="a557c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a557c-136">System.String</span></span>

## <span data-ttu-id="a557c-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a557c-137">OUTPUTS</span></span>

### <span data-ttu-id="a557c-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a557c-138">System.Boolean</span></span>

## <span data-ttu-id="a557c-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a557c-139">NOTES</span></span>

## <span data-ttu-id="a557c-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a557c-140">RELATED LINKS</span></span>
