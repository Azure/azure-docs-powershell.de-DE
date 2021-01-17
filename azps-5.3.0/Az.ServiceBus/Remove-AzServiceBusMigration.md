---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471881"
---
# <span data-ttu-id="fa630-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fa630-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="fa630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa630-102">SYNOPSIS</span></span>
<span data-ttu-id="fa630-103">Cmdlet löscht die Migrationskonfiguration für Standard- zu Premium-Namespaces</span><span class="sxs-lookup"><span data-stu-id="fa630-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="fa630-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa630-104">SYNTAX</span></span>

### <span data-ttu-id="fa630-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa630-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa630-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa630-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa630-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa630-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa630-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa630-108">DESCRIPTION</span></span>
<span data-ttu-id="fa630-109">Das **Cmdlet "Remove-AzServiceBusMigration"** löscht die Migrationskonfiguration für Standard- zu Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="fa630-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="fa630-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa630-110">EXAMPLES</span></span>

### <span data-ttu-id="fa630-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa630-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="fa630-112">Löscht die Migrationskonfiguration "TestingNamespaceStandardMigration".</span><span class="sxs-lookup"><span data-stu-id="fa630-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="fa630-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa630-113">PARAMETERS</span></span>

### <span data-ttu-id="fa630-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa630-114">-AsJob</span></span>
<span data-ttu-id="fa630-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fa630-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa630-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa630-116">-DefaultProfile</span></span>
<span data-ttu-id="fa630-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa630-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa630-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa630-118">-InputObject</span></span>
<span data-ttu-id="fa630-119">Service Bus Migration Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="fa630-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="fa630-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fa630-120">-Name</span></span>
<span data-ttu-id="fa630-121">Standardnamespacename</span><span class="sxs-lookup"><span data-stu-id="fa630-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="fa630-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa630-122">-PassThru</span></span>
<span data-ttu-id="fa630-123">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="fa630-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fa630-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa630-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa630-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="fa630-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa630-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa630-126">-ResourceId</span></span>
<span data-ttu-id="fa630-127">Service Bus Migration Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="fa630-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="fa630-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa630-128">-Confirm</span></span>
<span data-ttu-id="fa630-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa630-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa630-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fa630-130">-WhatIf</span></span>
<span data-ttu-id="fa630-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa630-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa630-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa630-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa630-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa630-133">CommonParameters</span></span>
<span data-ttu-id="fa630-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa630-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa630-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa630-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa630-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa630-136">INPUTS</span></span>

### <span data-ttu-id="fa630-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fa630-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="fa630-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fa630-138">System.String</span></span>

## <span data-ttu-id="fa630-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa630-139">OUTPUTS</span></span>

### <span data-ttu-id="fa630-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa630-140">System.Boolean</span></span>

## <span data-ttu-id="fa630-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fa630-141">NOTES</span></span>

## <span data-ttu-id="fa630-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fa630-142">RELATED LINKS</span></span>
