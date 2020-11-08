---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166855"
---
# <span data-ttu-id="2c22f-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2c22f-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="2c22f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c22f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c22f-103">Cmdlet löscht die Migrations Konfiguration für Standard mäßige in Premium-Namespaces</span><span class="sxs-lookup"><span data-stu-id="2c22f-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="2c22f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c22f-104">SYNTAX</span></span>

### <span data-ttu-id="2c22f-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c22f-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c22f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2c22f-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c22f-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c22f-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c22f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c22f-108">DESCRIPTION</span></span>
<span data-ttu-id="2c22f-109">Das Cmdlet **Remove-AzServiceBusMigration** löscht die Migrations Konfiguration für Standard-zu-Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="2c22f-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="2c22f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c22f-110">EXAMPLES</span></span>

### <span data-ttu-id="2c22f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c22f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="2c22f-112">Löscht die Migrations Konfiguration "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="2c22f-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="2c22f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c22f-113">PARAMETERS</span></span>

### <span data-ttu-id="2c22f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c22f-114">-AsJob</span></span>
<span data-ttu-id="2c22f-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2c22f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c22f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c22f-116">-DefaultProfile</span></span>
<span data-ttu-id="2c22f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c22f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c22f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c22f-118">-InputObject</span></span>
<span data-ttu-id="2c22f-119">Standard Namespace Objekt für ServiceBus-Migration</span><span class="sxs-lookup"><span data-stu-id="2c22f-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="2c22f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2c22f-120">-Name</span></span>
<span data-ttu-id="2c22f-121">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="2c22f-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="2c22f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c22f-122">-PassThru</span></span>
<span data-ttu-id="2c22f-123">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2c22f-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2c22f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c22f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2c22f-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2c22f-125">Resource Group Name</span></span>

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

### <span data-ttu-id="2c22f-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2c22f-126">-ResourceId</span></span>
<span data-ttu-id="2c22f-127">Service Bus-Migrations Standard-Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2c22f-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="2c22f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2c22f-128">-Confirm</span></span>
<span data-ttu-id="2c22f-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c22f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c22f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c22f-130">-WhatIf</span></span>
<span data-ttu-id="2c22f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c22f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c22f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c22f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c22f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c22f-133">CommonParameters</span></span>
<span data-ttu-id="2c22f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c22f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c22f-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c22f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c22f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c22f-136">INPUTS</span></span>

### <span data-ttu-id="2c22f-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2c22f-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="2c22f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2c22f-138">System.String</span></span>

## <span data-ttu-id="2c22f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c22f-139">OUTPUTS</span></span>

### <span data-ttu-id="2c22f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c22f-140">System.Boolean</span></span>

## <span data-ttu-id="2c22f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c22f-141">NOTES</span></span>

## <span data-ttu-id="2c22f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c22f-142">RELATED LINKS</span></span>
