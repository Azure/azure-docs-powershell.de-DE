---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003962"
---
# <span data-ttu-id="19c5b-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="19c5b-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="19c5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="19c5b-103">Cmdlets setzen die Migration von Standard-zu Premium-Namespace als abgeschlossen fest, und Verbindungszeichenfolgen des Standardnamespace verweisen nun auf den Premium-Namespace.</span><span class="sxs-lookup"><span data-stu-id="19c5b-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="19c5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19c5b-104">SYNTAX</span></span>

### <span data-ttu-id="19c5b-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="19c5b-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19c5b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="19c5b-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19c5b-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19c5b-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c5b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19c5b-108">DESCRIPTION</span></span>
<span data-ttu-id="19c5b-109">Die **vollständigen AzServiceBusMigration-** Cmdlets setzen die Migration von Standard-zu Premium-Namespace als abgeschlossen fest, und Verbindungszeichenfolgen des Standardnamespace verweisen nun auf den Premium-Namespace.</span><span class="sxs-lookup"><span data-stu-id="19c5b-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="19c5b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19c5b-110">EXAMPLES</span></span>

### <span data-ttu-id="19c5b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19c5b-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="19c5b-112">Legt die Migration des Namespace "NamespaceStandardMigration" als abgeschlossen fest.</span><span class="sxs-lookup"><span data-stu-id="19c5b-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="19c5b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="19c5b-113">PARAMETERS</span></span>

### <span data-ttu-id="19c5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c5b-114">-DefaultProfile</span></span>
<span data-ttu-id="19c5b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19c5b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c5b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="19c5b-116">-InputObject</span></span>
<span data-ttu-id="19c5b-117">Service Bus-Migrations Konfiguration – Standard Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="19c5b-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="19c5b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="19c5b-118">-Name</span></span>
<span data-ttu-id="19c5b-119">Standard Namespace Name</span><span class="sxs-lookup"><span data-stu-id="19c5b-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="19c5b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19c5b-120">-PassThru</span></span>
<span data-ttu-id="19c5b-121">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="19c5b-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="19c5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c5b-122">-ResourceGroupName</span></span>
<span data-ttu-id="19c5b-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="19c5b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="19c5b-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="19c5b-124">-ResourceId</span></span>
<span data-ttu-id="19c5b-125">Service Bus-Migration – Standard Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="19c5b-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="19c5b-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19c5b-126">-Confirm</span></span>
<span data-ttu-id="19c5b-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19c5b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c5b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c5b-128">-WhatIf</span></span>
<span data-ttu-id="19c5b-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19c5b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c5b-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19c5b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c5b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c5b-131">CommonParameters</span></span>
<span data-ttu-id="19c5b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c5b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c5b-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c5b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c5b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19c5b-134">INPUTS</span></span>

### <span data-ttu-id="19c5b-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="19c5b-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="19c5b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="19c5b-136">System.String</span></span>

## <span data-ttu-id="19c5b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19c5b-137">OUTPUTS</span></span>

### <span data-ttu-id="19c5b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19c5b-138">System.Boolean</span></span>

## <span data-ttu-id="19c5b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="19c5b-139">NOTES</span></span>

## <span data-ttu-id="19c5b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19c5b-140">RELATED LINKS</span></span>
