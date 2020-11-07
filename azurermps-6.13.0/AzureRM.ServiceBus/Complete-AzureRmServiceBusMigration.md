---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/complete-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
ms.openlocfilehash: 0006e4768dc27994d18e93e48696b5ee9a514c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664005"
---
# <span data-ttu-id="ec36f-101">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ec36f-101">Complete-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="ec36f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec36f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec36f-103">Cmdlets setzen die Migration von Standard-zu Premium-Namespace als abgeschlossen fest, und Verbindungszeichenfolgen des Standardnamespace verweisen nun auf den Premium-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ec36f-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec36f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec36f-104">SYNTAX</span></span>

### <span data-ttu-id="ec36f-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec36f-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec36f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ec36f-106">NamespaceInputObjectSet</span></span>
```
Complete-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec36f-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec36f-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec36f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec36f-108">DESCRIPTION</span></span>
<span data-ttu-id="ec36f-109">Die **vollständigen AzureRmServiceBusMigration-** Cmdlets setzen die Migration von Standard-zu Premium-Namespace als abgeschlossen fest, und Verbindungszeichenfolgen des Standardnamespace verweisen nun auf den Premium-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ec36f-109">The **Complete-AzureRmServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="ec36f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec36f-110">EXAMPLES</span></span>

### <span data-ttu-id="ec36f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec36f-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="ec36f-112">Legt die Migration des Namespace "NamespaceStandardMirgation" als abgeschlossen fest.</span><span class="sxs-lookup"><span data-stu-id="ec36f-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="ec36f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec36f-113">PARAMETERS</span></span>

### <span data-ttu-id="ec36f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec36f-114">-DefaultProfile</span></span>
<span data-ttu-id="ec36f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec36f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec36f-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ec36f-116">-InputObject</span></span>
<span data-ttu-id="ec36f-117">Service Bus-Migrations Konfiguration – Standard Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="ec36f-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="ec36f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ec36f-118">-Name</span></span>
<span data-ttu-id="ec36f-119">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ec36f-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="ec36f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec36f-120">-PassThru</span></span>
<span data-ttu-id="ec36f-121">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ec36f-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ec36f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec36f-122">-ResourceGroupName</span></span>
<span data-ttu-id="ec36f-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ec36f-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ec36f-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ec36f-124">-ResourceId</span></span>
<span data-ttu-id="ec36f-125">ServiceBus-Migratio-Standard Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ec36f-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="ec36f-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec36f-126">-Confirm</span></span>
<span data-ttu-id="ec36f-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec36f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec36f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec36f-128">-WhatIf</span></span>
<span data-ttu-id="ec36f-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec36f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec36f-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec36f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec36f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec36f-131">CommonParameters</span></span>
<span data-ttu-id="ec36f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec36f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec36f-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec36f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec36f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec36f-134">INPUTS</span></span>

### <span data-ttu-id="ec36f-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ec36f-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="ec36f-136">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ec36f-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ec36f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ec36f-137">System.String</span></span>

## <span data-ttu-id="ec36f-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec36f-138">OUTPUTS</span></span>

### <span data-ttu-id="ec36f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec36f-139">System.Boolean</span></span>

## <span data-ttu-id="ec36f-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec36f-140">NOTES</span></span>

## <span data-ttu-id="ec36f-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec36f-141">RELATED LINKS</span></span>
