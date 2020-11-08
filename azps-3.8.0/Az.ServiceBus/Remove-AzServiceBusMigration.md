---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995995"
---
# <span data-ttu-id="0ebf3-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0ebf3-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="0ebf3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ebf3-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebf3-103">Cmdlet löscht die Migrations Konfiguration für Standard mäßige in Premium-Namespaces</span><span class="sxs-lookup"><span data-stu-id="0ebf3-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="0ebf3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ebf3-104">SYNTAX</span></span>

### <span data-ttu-id="0ebf3-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ebf3-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ebf3-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0ebf3-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ebf3-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ebf3-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ebf3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ebf3-108">DESCRIPTION</span></span>
<span data-ttu-id="0ebf3-109">Das Cmdlet **Remove-AzServiceBusMigration** löscht die Migrations Konfiguration für Standard-zu-Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="0ebf3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ebf3-110">EXAMPLES</span></span>

### <span data-ttu-id="0ebf3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ebf3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="0ebf3-112">Löscht die Migrations Konfiguration "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="0ebf3-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="0ebf3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ebf3-113">PARAMETERS</span></span>

### <span data-ttu-id="0ebf3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ebf3-114">-AsJob</span></span>
<span data-ttu-id="0ebf3-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0ebf3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ebf3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebf3-116">-DefaultProfile</span></span>
<span data-ttu-id="0ebf3-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebf3-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0ebf3-118">-InputObject</span></span>
<span data-ttu-id="0ebf3-119">Standard Namespace Objekt für ServiceBus-Migration</span><span class="sxs-lookup"><span data-stu-id="0ebf3-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="0ebf3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0ebf3-120">-Name</span></span>
<span data-ttu-id="0ebf3-121">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="0ebf3-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="0ebf3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ebf3-122">-PassThru</span></span>
<span data-ttu-id="0ebf3-123">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0ebf3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebf3-124">-ResourceGroupName</span></span>
<span data-ttu-id="0ebf3-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0ebf3-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0ebf3-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0ebf3-126">-ResourceId</span></span>
<span data-ttu-id="0ebf3-127">Service Bus-Migrations Standard-Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0ebf3-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="0ebf3-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ebf3-128">-Confirm</span></span>
<span data-ttu-id="0ebf3-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ebf3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ebf3-130">-WhatIf</span></span>
<span data-ttu-id="0ebf3-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ebf3-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ebf3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebf3-133">CommonParameters</span></span>
<span data-ttu-id="0ebf3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebf3-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebf3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebf3-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ebf3-136">INPUTS</span></span>

### <span data-ttu-id="0ebf3-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0ebf3-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="0ebf3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0ebf3-138">System.String</span></span>

## <span data-ttu-id="0ebf3-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ebf3-139">OUTPUTS</span></span>

### <span data-ttu-id="0ebf3-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ebf3-140">System.Boolean</span></span>

## <span data-ttu-id="0ebf3-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ebf3-141">NOTES</span></span>

## <span data-ttu-id="0ebf3-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ebf3-142">RELATED LINKS</span></span>
