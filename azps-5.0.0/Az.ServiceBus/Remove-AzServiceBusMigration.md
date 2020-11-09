---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300153"
---
# <span data-ttu-id="c9ed1-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c9ed1-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="c9ed1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ed1-103">Cmdlet löscht die Migrations Konfiguration für Standard mäßige in Premium-Namespaces</span><span class="sxs-lookup"><span data-stu-id="c9ed1-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="c9ed1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9ed1-104">SYNTAX</span></span>

### <span data-ttu-id="c9ed1-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9ed1-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9ed1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c9ed1-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9ed1-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9ed1-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9ed1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9ed1-108">DESCRIPTION</span></span>
<span data-ttu-id="c9ed1-109">Das Cmdlet **Remove-AzServiceBusMigration** löscht die Migrations Konfiguration für Standard-zu-Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="c9ed1-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="c9ed1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9ed1-110">EXAMPLES</span></span>

### <span data-ttu-id="c9ed1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c9ed1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="c9ed1-112">Löscht die Migrations Konfiguration "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="c9ed1-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="c9ed1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9ed1-113">PARAMETERS</span></span>

### <span data-ttu-id="c9ed1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9ed1-114">-AsJob</span></span>
<span data-ttu-id="c9ed1-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c9ed1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9ed1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ed1-116">-DefaultProfile</span></span>
<span data-ttu-id="c9ed1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9ed1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9ed1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c9ed1-118">-InputObject</span></span>
<span data-ttu-id="c9ed1-119">Standard Namespace Objekt für ServiceBus-Migration</span><span class="sxs-lookup"><span data-stu-id="c9ed1-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="c9ed1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c9ed1-120">-Name</span></span>
<span data-ttu-id="c9ed1-121">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="c9ed1-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="c9ed1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9ed1-122">-PassThru</span></span>
<span data-ttu-id="c9ed1-123">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c9ed1-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c9ed1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ed1-124">-ResourceGroupName</span></span>
<span data-ttu-id="c9ed1-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c9ed1-125">Resource Group Name</span></span>

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

### <span data-ttu-id="c9ed1-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c9ed1-126">-ResourceId</span></span>
<span data-ttu-id="c9ed1-127">Service Bus-Migrations Standard-Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c9ed1-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="c9ed1-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9ed1-128">-Confirm</span></span>
<span data-ttu-id="c9ed1-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9ed1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9ed1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9ed1-130">-WhatIf</span></span>
<span data-ttu-id="c9ed1-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9ed1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9ed1-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9ed1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9ed1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ed1-133">CommonParameters</span></span>
<span data-ttu-id="c9ed1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ed1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ed1-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ed1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ed1-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9ed1-136">INPUTS</span></span>

### <span data-ttu-id="c9ed1-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c9ed1-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="c9ed1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c9ed1-138">System.String</span></span>

## <span data-ttu-id="c9ed1-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9ed1-139">OUTPUTS</span></span>

### <span data-ttu-id="c9ed1-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9ed1-140">System.Boolean</span></span>

## <span data-ttu-id="c9ed1-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9ed1-141">NOTES</span></span>

## <span data-ttu-id="c9ed1-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9ed1-142">RELATED LINKS</span></span>
