---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293279"
---
# <span data-ttu-id="6fe60-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6fe60-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="6fe60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe60-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe60-103">Cmdlet löscht die Migrationskonfiguration für Standard- zu Premium-Namespaces</span><span class="sxs-lookup"><span data-stu-id="6fe60-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="6fe60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fe60-104">SYNTAX</span></span>

### <span data-ttu-id="6fe60-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6fe60-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe60-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6fe60-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe60-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fe60-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fe60-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fe60-108">DESCRIPTION</span></span>
<span data-ttu-id="6fe60-109">Das **Cmdlet "Remove-AzServiceBusMigration"** löscht die Migrationskonfiguration für Standard- zu Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="6fe60-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="6fe60-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6fe60-110">EXAMPLES</span></span>

### <span data-ttu-id="6fe60-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6fe60-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="6fe60-112">Löscht die Migrationskonfiguration "TestingNamespaceStandardMigration".</span><span class="sxs-lookup"><span data-stu-id="6fe60-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="6fe60-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fe60-113">PARAMETERS</span></span>

### <span data-ttu-id="6fe60-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fe60-114">-AsJob</span></span>
<span data-ttu-id="6fe60-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6fe60-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fe60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe60-116">-DefaultProfile</span></span>
<span data-ttu-id="6fe60-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fe60-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fe60-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fe60-118">-InputObject</span></span>
<span data-ttu-id="6fe60-119">Service Bus Migration Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="6fe60-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="6fe60-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6fe60-120">-Name</span></span>
<span data-ttu-id="6fe60-121">Standardnamespacename</span><span class="sxs-lookup"><span data-stu-id="6fe60-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="6fe60-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fe60-122">-PassThru</span></span>
<span data-ttu-id="6fe60-123">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="6fe60-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6fe60-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe60-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fe60-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="6fe60-125">Resource Group Name</span></span>

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

### <span data-ttu-id="6fe60-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fe60-126">-ResourceId</span></span>
<span data-ttu-id="6fe60-127">Service Bus Migration Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="6fe60-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="6fe60-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fe60-128">-Confirm</span></span>
<span data-ttu-id="6fe60-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fe60-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe60-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6fe60-130">-WhatIf</span></span>
<span data-ttu-id="6fe60-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fe60-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe60-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fe60-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe60-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe60-133">CommonParameters</span></span>
<span data-ttu-id="6fe60-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe60-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe60-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe60-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe60-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6fe60-136">INPUTS</span></span>

### <span data-ttu-id="6fe60-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6fe60-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="6fe60-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6fe60-138">System.String</span></span>

## <span data-ttu-id="6fe60-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6fe60-139">OUTPUTS</span></span>

### <span data-ttu-id="6fe60-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6fe60-140">System.Boolean</span></span>

## <span data-ttu-id="6fe60-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6fe60-141">NOTES</span></span>

## <span data-ttu-id="6fe60-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6fe60-142">RELATED LINKS</span></span>
