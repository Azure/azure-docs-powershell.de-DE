---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004512"
---
# <span data-ttu-id="cdd62-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="cdd62-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="cdd62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdd62-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd62-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="cdd62-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="cdd62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdd62-104">SYNTAX</span></span>

### <span data-ttu-id="cdd62-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cdd62-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd62-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cdd62-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd62-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdd62-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd62-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdd62-108">DESCRIPTION</span></span>
<span data-ttu-id="cdd62-109">Die **AzServiceBusMigration-** Cmdlets beenden die Migration zwischen dem Standard-zu-Premium-Namespace</span><span class="sxs-lookup"><span data-stu-id="cdd62-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="cdd62-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdd62-110">EXAMPLES</span></span>

### <span data-ttu-id="cdd62-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cdd62-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="cdd62-112">Das Cmdlet beendet die Migration zwischen dem Standard Namespace und dem Premium Namespace, der beim Erstellen der Migrations Konfiguration bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cdd62-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="cdd62-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdd62-113">PARAMETERS</span></span>

### <span data-ttu-id="cdd62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd62-114">-DefaultProfile</span></span>
<span data-ttu-id="cdd62-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdd62-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd62-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cdd62-116">-InputObject</span></span>
<span data-ttu-id="cdd62-117">Standard Namespace Objekt für die ServiceBus-Migrations Konfiguration</span><span class="sxs-lookup"><span data-stu-id="cdd62-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="cdd62-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cdd62-118">-Name</span></span>
<span data-ttu-id="cdd62-119">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="cdd62-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="cdd62-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdd62-120">-PassThru</span></span>
<span data-ttu-id="cdd62-121">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="cdd62-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="cdd62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd62-122">-ResourceGroupName</span></span>
<span data-ttu-id="cdd62-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="cdd62-123">Resource Group Name</span></span>

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

### <span data-ttu-id="cdd62-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cdd62-124">-ResourceId</span></span>
<span data-ttu-id="cdd62-125">Standard mäßige Namespace-Ressourcen-ID für die ServiceBus-Migrations Konfiguration</span><span class="sxs-lookup"><span data-stu-id="cdd62-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="cdd62-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cdd62-126">-Confirm</span></span>
<span data-ttu-id="cdd62-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cdd62-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd62-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd62-128">-WhatIf</span></span>
<span data-ttu-id="cdd62-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdd62-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd62-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cdd62-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd62-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd62-131">CommonParameters</span></span>
<span data-ttu-id="cdd62-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd62-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd62-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdd62-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd62-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdd62-134">INPUTS</span></span>

### <span data-ttu-id="cdd62-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cdd62-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="cdd62-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cdd62-136">System.String</span></span>

## <span data-ttu-id="cdd62-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdd62-137">OUTPUTS</span></span>

### <span data-ttu-id="cdd62-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdd62-138">System.Boolean</span></span>

## <span data-ttu-id="cdd62-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdd62-139">NOTES</span></span>

## <span data-ttu-id="cdd62-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdd62-140">RELATED LINKS</span></span>
