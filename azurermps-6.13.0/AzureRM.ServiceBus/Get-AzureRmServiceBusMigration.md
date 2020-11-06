---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
ms.openlocfilehash: cdf869f13c90982c40568f37c0757ef2e7547b3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497334"
---
# <span data-ttu-id="a1f8c-101">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a1f8c-101">Get-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="a1f8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f8c-103">Ruft MigrationConfiguration für den Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="a1f8c-103">Retrieves MigrationConfiguration for the namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1f8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1f8c-104">SYNTAX</span></span>

### <span data-ttu-id="a1f8c-105">MigrationConfigurationPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1f8c-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1f8c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1f8c-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusMigration [-InputObject] <PSNamespaceAttributes>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1f8c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1f8c-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1f8c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f8c-108">DESCRIPTION</span></span>
<span data-ttu-id="a1f8c-109">Die **Get-AzureRmServiceBusMigration** Ruft die Migrations Konfiguration für den Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="a1f8c-109">The **Get-AzureRmServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="a1f8c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1f8c-110">EXAMPLES</span></span>

### <span data-ttu-id="a1f8c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1f8c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="a1f8c-112">Ruft die Migrations Konfigurationseigenschaften von "TestingNamespaceStandardMirgation" ab.</span><span class="sxs-lookup"><span data-stu-id="a1f8c-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="a1f8c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1f8c-113">PARAMETERS</span></span>

### <span data-ttu-id="a1f8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f8c-114">-DefaultProfile</span></span>
<span data-ttu-id="a1f8c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1f8c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1f8c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a1f8c-116">-InputObject</span></span>
<span data-ttu-id="a1f8c-117">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="a1f8c-117">Namespace Object</span></span>

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

### <span data-ttu-id="a1f8c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a1f8c-118">-Name</span></span>
<span data-ttu-id="a1f8c-119">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a1f8c-119">Namespace Name</span></span>

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

### <span data-ttu-id="a1f8c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f8c-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1f8c-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a1f8c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a1f8c-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a1f8c-122">-ResourceId</span></span>
<span data-ttu-id="a1f8c-123">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a1f8c-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="a1f8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f8c-124">CommonParameters</span></span>
<span data-ttu-id="a1f8c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f8c-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1f8c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f8c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1f8c-127">INPUTS</span></span>

### <span data-ttu-id="a1f8c-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a1f8c-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="a1f8c-129">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a1f8c-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a1f8c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a1f8c-130">System.String</span></span>

## <span data-ttu-id="a1f8c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1f8c-131">OUTPUTS</span></span>

### <span data-ttu-id="a1f8c-132">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a1f8c-132">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="a1f8c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1f8c-133">NOTES</span></span>

## <span data-ttu-id="a1f8c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1f8c-134">RELATED LINKS</span></span>
