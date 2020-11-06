---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
ms.openlocfilehash: c378f6315f66b7149c1a8bb6d51ce806425065a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482038"
---
# <span data-ttu-id="04dba-101">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="04dba-101">Remove-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="04dba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04dba-102">SYNOPSIS</span></span>
<span data-ttu-id="04dba-103">Cmdlet löscht die Migrations Konfiguration für Standard mäßige in Premium-Namespaces</span><span class="sxs-lookup"><span data-stu-id="04dba-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04dba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04dba-104">SYNTAX</span></span>

### <span data-ttu-id="04dba-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="04dba-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04dba-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="04dba-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04dba-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04dba-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04dba-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04dba-108">DESCRIPTION</span></span>
<span data-ttu-id="04dba-109">Das Cmdlet **Remove-AzureRmServiceBusMigration** löscht die Migrations Konfiguration für Standard-zu-Premium-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="04dba-109">The **Remove-AzureRmServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="04dba-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04dba-110">EXAMPLES</span></span>

### <span data-ttu-id="04dba-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04dba-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="04dba-112">Löscht die Migrations Konfiguration "TestingNamespaceStandardMirgation"</span><span class="sxs-lookup"><span data-stu-id="04dba-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="04dba-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="04dba-113">PARAMETERS</span></span>

### <span data-ttu-id="04dba-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04dba-114">-AsJob</span></span>
<span data-ttu-id="04dba-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="04dba-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04dba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04dba-116">-DefaultProfile</span></span>
<span data-ttu-id="04dba-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04dba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04dba-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="04dba-118">-InputObject</span></span>
<span data-ttu-id="04dba-119">Standard Namespace Objekt für ServiceBus-Migration</span><span class="sxs-lookup"><span data-stu-id="04dba-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="04dba-120">-Name</span><span class="sxs-lookup"><span data-stu-id="04dba-120">-Name</span></span>
<span data-ttu-id="04dba-121">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="04dba-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="04dba-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04dba-122">-PassThru</span></span>
<span data-ttu-id="04dba-123">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="04dba-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="04dba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04dba-124">-ResourceGroupName</span></span>
<span data-ttu-id="04dba-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="04dba-125">Resource Group Name</span></span>

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

### <span data-ttu-id="04dba-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="04dba-126">-ResourceId</span></span>
<span data-ttu-id="04dba-127">Service Bus-Migrations Standard-Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="04dba-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="04dba-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04dba-128">-Confirm</span></span>
<span data-ttu-id="04dba-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04dba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04dba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04dba-130">-WhatIf</span></span>
<span data-ttu-id="04dba-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04dba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04dba-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04dba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04dba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04dba-133">CommonParameters</span></span>
<span data-ttu-id="04dba-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04dba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04dba-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04dba-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04dba-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04dba-136">INPUTS</span></span>

### <span data-ttu-id="04dba-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="04dba-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="04dba-138">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="04dba-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="04dba-139">System. String</span><span class="sxs-lookup"><span data-stu-id="04dba-139">System.String</span></span>

## <span data-ttu-id="04dba-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04dba-140">OUTPUTS</span></span>

### <span data-ttu-id="04dba-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04dba-141">System.Boolean</span></span>

## <span data-ttu-id="04dba-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="04dba-142">NOTES</span></span>

## <span data-ttu-id="04dba-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04dba-143">RELATED LINKS</span></span>
