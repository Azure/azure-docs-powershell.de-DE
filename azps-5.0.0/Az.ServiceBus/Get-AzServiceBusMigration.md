---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180148"
---
# <span data-ttu-id="4ae7b-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="4ae7b-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="4ae7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ae7b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae7b-103">Ruft MigrationConfiguration für den Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="4ae7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ae7b-104">SYNTAX</span></span>

### <span data-ttu-id="4ae7b-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ae7b-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ae7b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ae7b-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ae7b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ae7b-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ae7b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ae7b-108">DESCRIPTION</span></span>
<span data-ttu-id="4ae7b-109">Die **Get-AzServiceBusMigration** Ruft die Migrations Konfiguration für den Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="4ae7b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ae7b-110">EXAMPLES</span></span>

### <span data-ttu-id="4ae7b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ae7b-111">Example 1</span></span>
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

<span data-ttu-id="4ae7b-112">Ruft die Migrations Konfigurationseigenschaften von "TestingNamespaceStandardMigration" ab.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="4ae7b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ae7b-113">PARAMETERS</span></span>

### <span data-ttu-id="4ae7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae7b-114">-DefaultProfile</span></span>
<span data-ttu-id="4ae7b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ae7b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ae7b-116">-InputObject</span></span>
<span data-ttu-id="4ae7b-117">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="4ae7b-117">Namespace Object</span></span>

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

### <span data-ttu-id="4ae7b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4ae7b-118">-Name</span></span>
<span data-ttu-id="4ae7b-119">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4ae7b-119">Namespace Name</span></span>

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

### <span data-ttu-id="4ae7b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae7b-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ae7b-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="4ae7b-121">Resource Group Name</span></span>

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

### <span data-ttu-id="4ae7b-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4ae7b-122">-ResourceId</span></span>
<span data-ttu-id="4ae7b-123">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4ae7b-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="4ae7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae7b-124">CommonParameters</span></span>
<span data-ttu-id="4ae7b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae7b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ae7b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae7b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ae7b-127">INPUTS</span></span>

### <span data-ttu-id="4ae7b-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4ae7b-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="4ae7b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4ae7b-129">System.String</span></span>

## <span data-ttu-id="4ae7b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ae7b-130">OUTPUTS</span></span>

### <span data-ttu-id="4ae7b-131">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="4ae7b-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="4ae7b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ae7b-132">NOTES</span></span>

## <span data-ttu-id="4ae7b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ae7b-133">RELATED LINKS</span></span>
