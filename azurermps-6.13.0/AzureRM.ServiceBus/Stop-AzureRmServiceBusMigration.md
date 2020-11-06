---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/stop-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
ms.openlocfilehash: 25a8b6918c5cd10a2f47230274c357008731ffba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497305"
---
# <span data-ttu-id="64811-101">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="64811-101">Stop-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="64811-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64811-102">SYNOPSIS</span></span>
<span data-ttu-id="64811-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="64811-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64811-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64811-104">SYNTAX</span></span>

### <span data-ttu-id="64811-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="64811-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64811-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="64811-106">NamespaceInputObjectSet</span></span>
```
Stop-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64811-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64811-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64811-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64811-108">DESCRIPTION</span></span>
<span data-ttu-id="64811-109">Die Cmdlets " **Stop-AzureRmServiceBusMigration** " tremitates die Migration zwischen dem Standard-zu-Premium-Namespace</span><span class="sxs-lookup"><span data-stu-id="64811-109">The **Stop-AzureRmServiceBusMigration** cmdlets  tremitates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="64811-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64811-110">EXAMPLES</span></span>

### <span data-ttu-id="64811-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64811-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="64811-112">Cmdlet termitates die Migration zwischen dem Standard Namespace und dem Premium Namespace, der beim Erstellen der Migrations Konfiguration bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="64811-112">cmdlet termitates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="64811-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="64811-113">PARAMETERS</span></span>

### <span data-ttu-id="64811-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64811-114">-DefaultProfile</span></span>
<span data-ttu-id="64811-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64811-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64811-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64811-116">-InputObject</span></span>
<span data-ttu-id="64811-117">Standard Namespace Objekt für die ServiceBus-Migrations Konfiguration</span><span class="sxs-lookup"><span data-stu-id="64811-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="64811-118">-Name</span><span class="sxs-lookup"><span data-stu-id="64811-118">-Name</span></span>
<span data-ttu-id="64811-119">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="64811-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="64811-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64811-120">-PassThru</span></span>
<span data-ttu-id="64811-121">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="64811-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="64811-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64811-122">-ResourceGroupName</span></span>
<span data-ttu-id="64811-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="64811-123">Resource Group Name</span></span>

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

### <span data-ttu-id="64811-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="64811-124">-ResourceId</span></span>
<span data-ttu-id="64811-125">Standard mäßige Namespace-Ressourcen-ID für die ServiceBus-Migrations Konfiguration</span><span class="sxs-lookup"><span data-stu-id="64811-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="64811-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64811-126">-Confirm</span></span>
<span data-ttu-id="64811-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64811-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64811-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64811-128">-WhatIf</span></span>
<span data-ttu-id="64811-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64811-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64811-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64811-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64811-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64811-131">CommonParameters</span></span>
<span data-ttu-id="64811-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64811-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64811-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64811-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64811-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64811-134">INPUTS</span></span>

### <span data-ttu-id="64811-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="64811-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="64811-136">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="64811-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="64811-137">System. String</span><span class="sxs-lookup"><span data-stu-id="64811-137">System.String</span></span>

## <span data-ttu-id="64811-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64811-138">OUTPUTS</span></span>

### <span data-ttu-id="64811-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64811-139">System.Boolean</span></span>

## <span data-ttu-id="64811-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="64811-140">NOTES</span></span>

## <span data-ttu-id="64811-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64811-141">RELATED LINKS</span></span>
