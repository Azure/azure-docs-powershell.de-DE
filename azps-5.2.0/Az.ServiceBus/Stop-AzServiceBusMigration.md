---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369072"
---
# <span data-ttu-id="8a0c0-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8a0c0-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="8a0c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a0c0-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0c0-103">{{Fill in the Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="8a0c0-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="8a0c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a0c0-104">SYNTAX</span></span>

### <span data-ttu-id="8a0c0-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a0c0-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a0c0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8a0c0-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a0c0-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a0c0-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a0c0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a0c0-108">DESCRIPTION</span></span>
<span data-ttu-id="8a0c0-109">Mit **den "Stop-AzServiceBusMigration"-Cmdlets** wird die Migration zwischen dem Standard- und dem Premiumnamespace beendet.</span><span class="sxs-lookup"><span data-stu-id="8a0c0-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="8a0c0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a0c0-110">EXAMPLES</span></span>

### <span data-ttu-id="8a0c0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a0c0-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="8a0c0-112">Das Cmdlet beendet die Migration zwischen standard-Namespace und Premium-Namespace, die beim Erstellen der Migrationskonfiguration bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8a0c0-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="8a0c0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a0c0-113">PARAMETERS</span></span>

### <span data-ttu-id="8a0c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a0c0-114">-DefaultProfile</span></span>
<span data-ttu-id="8a0c0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a0c0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a0c0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a0c0-116">-InputObject</span></span>
<span data-ttu-id="8a0c0-117">Service Bus Migration Configuration Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="8a0c0-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="8a0c0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8a0c0-118">-Name</span></span>
<span data-ttu-id="8a0c0-119">Standardnamespacename</span><span class="sxs-lookup"><span data-stu-id="8a0c0-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="8a0c0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a0c0-120">-PassThru</span></span>
<span data-ttu-id="8a0c0-121">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8a0c0-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8a0c0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0c0-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a0c0-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8a0c0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8a0c0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a0c0-124">-ResourceId</span></span>
<span data-ttu-id="8a0c0-125">Service Bus Migration Configuration Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="8a0c0-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="8a0c0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a0c0-126">-Confirm</span></span>
<span data-ttu-id="8a0c0-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a0c0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a0c0-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8a0c0-128">-WhatIf</span></span>
<span data-ttu-id="8a0c0-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a0c0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a0c0-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a0c0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a0c0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0c0-131">CommonParameters</span></span>
<span data-ttu-id="8a0c0-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a0c0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0c0-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a0c0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0c0-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a0c0-134">INPUTS</span></span>

### <span data-ttu-id="8a0c0-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8a0c0-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="8a0c0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8a0c0-136">System.String</span></span>

## <span data-ttu-id="8a0c0-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a0c0-137">OUTPUTS</span></span>

### <span data-ttu-id="8a0c0-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a0c0-138">System.Boolean</span></span>

## <span data-ttu-id="8a0c0-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8a0c0-139">NOTES</span></span>

## <span data-ttu-id="8a0c0-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8a0c0-140">RELATED LINKS</span></span>
