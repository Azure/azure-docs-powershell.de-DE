---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300251"
---
# <span data-ttu-id="2afa6-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2afa6-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="2afa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2afa6-102">SYNOPSIS</span></span>
<span data-ttu-id="2afa6-103">cmdlets set the Migration from Standard to Premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span><span class="sxs-lookup"><span data-stu-id="2afa6-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="2afa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2afa6-104">SYNTAX</span></span>

### <span data-ttu-id="2afa6-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2afa6-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afa6-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2afa6-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afa6-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2afa6-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2afa6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2afa6-108">DESCRIPTION</span></span>
<span data-ttu-id="2afa6-109">Mit **den Cmdlets "Complete-AzServiceBusMigration"** wird die Migration von Standard auf den Premiumnamespace als "complete" festgelegt, und Verbindungszeichenfolgen des Standardnamespaces verweisen jetzt auf den Premium-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2afa6-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="2afa6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2afa6-110">EXAMPLES</span></span>

### <span data-ttu-id="2afa6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2afa6-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="2afa6-112">Legt den Namespace "Migration of 'NamespaceStandardMigration' als abgeschlossen fest.</span><span class="sxs-lookup"><span data-stu-id="2afa6-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="2afa6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2afa6-113">PARAMETERS</span></span>

### <span data-ttu-id="2afa6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2afa6-114">-DefaultProfile</span></span>
<span data-ttu-id="2afa6-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2afa6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2afa6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2afa6-116">-InputObject</span></span>
<span data-ttu-id="2afa6-117">Service Bus Migration configuration - Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="2afa6-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="2afa6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2afa6-118">-Name</span></span>
<span data-ttu-id="2afa6-119">Standardnamespacename</span><span class="sxs-lookup"><span data-stu-id="2afa6-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="2afa6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2afa6-120">-PassThru</span></span>
<span data-ttu-id="2afa6-121">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2afa6-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2afa6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2afa6-122">-ResourceGroupName</span></span>
<span data-ttu-id="2afa6-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2afa6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2afa6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2afa6-124">-ResourceId</span></span>
<span data-ttu-id="2afa6-125">Service Bus Migration – Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="2afa6-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="2afa6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2afa6-126">-Confirm</span></span>
<span data-ttu-id="2afa6-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2afa6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2afa6-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2afa6-128">-WhatIf</span></span>
<span data-ttu-id="2afa6-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2afa6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2afa6-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2afa6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2afa6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2afa6-131">CommonParameters</span></span>
<span data-ttu-id="2afa6-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2afa6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2afa6-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2afa6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2afa6-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2afa6-134">INPUTS</span></span>

### <span data-ttu-id="2afa6-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2afa6-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="2afa6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2afa6-136">System.String</span></span>

## <span data-ttu-id="2afa6-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2afa6-137">OUTPUTS</span></span>

### <span data-ttu-id="2afa6-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2afa6-138">System.Boolean</span></span>

## <span data-ttu-id="2afa6-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2afa6-139">NOTES</span></span>

## <span data-ttu-id="2afa6-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2afa6-140">RELATED LINKS</span></span>
