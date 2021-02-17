---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165100"
---
# <span data-ttu-id="28b41-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="28b41-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="28b41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28b41-102">SYNOPSIS</span></span>
<span data-ttu-id="28b41-103">Ruft die MigrationConfiguration für den Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="28b41-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="28b41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28b41-104">SYNTAX</span></span>

### <span data-ttu-id="28b41-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="28b41-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28b41-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="28b41-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28b41-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28b41-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28b41-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28b41-108">DESCRIPTION</span></span>
<span data-ttu-id="28b41-109">**Get-AzServiceBusMigration** ruft die Migrationskonfiguration für den Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="28b41-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="28b41-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28b41-110">EXAMPLES</span></span>

### <span data-ttu-id="28b41-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28b41-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="28b41-112">Ruft die Migrationskonfigurationseigenschaften von 'TestingNamespaceStandardMigration' ab</span><span class="sxs-lookup"><span data-stu-id="28b41-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="28b41-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28b41-113">PARAMETERS</span></span>

### <span data-ttu-id="28b41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b41-114">-DefaultProfile</span></span>
<span data-ttu-id="28b41-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28b41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28b41-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28b41-116">-InputObject</span></span>
<span data-ttu-id="28b41-117">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="28b41-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28b41-118">-Name</span><span class="sxs-lookup"><span data-stu-id="28b41-118">-Name</span></span>
<span data-ttu-id="28b41-119">Namespacename</span><span class="sxs-lookup"><span data-stu-id="28b41-119">Namespace Name</span></span>

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

### <span data-ttu-id="28b41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b41-120">-ResourceGroupName</span></span>
<span data-ttu-id="28b41-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="28b41-121">Resource Group Name</span></span>

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

### <span data-ttu-id="28b41-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28b41-122">-ResourceId</span></span>
<span data-ttu-id="28b41-123">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="28b41-123">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b41-124">CommonParameters</span></span>
<span data-ttu-id="28b41-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b41-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b41-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b41-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28b41-127">INPUTS</span></span>

### <span data-ttu-id="28b41-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="28b41-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="28b41-129">System.String</span><span class="sxs-lookup"><span data-stu-id="28b41-129">System.String</span></span>

## <span data-ttu-id="28b41-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28b41-130">OUTPUTS</span></span>

### <span data-ttu-id="28b41-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="28b41-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="28b41-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="28b41-132">NOTES</span></span>

## <span data-ttu-id="28b41-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="28b41-133">RELATED LINKS</span></span>
