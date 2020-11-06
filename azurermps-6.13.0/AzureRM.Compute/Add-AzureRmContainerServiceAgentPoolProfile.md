---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: eb2b4e1ea50c7dd8e175583835d16c791313db6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502218"
---
# <span data-ttu-id="15072-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="15072-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="15072-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15072-102">SYNOPSIS</span></span>
<span data-ttu-id="15072-103">Fügt ein Pool Profil für Containerdienst-Agents hinzu.</span><span class="sxs-lookup"><span data-stu-id="15072-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15072-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15072-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15072-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15072-105">DESCRIPTION</span></span>
<span data-ttu-id="15072-106">Mit dem Cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** wird ein Containerdienst-Agent-Pool Profil zu einem lokalen Containerdienst Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="15072-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="15072-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15072-107">EXAMPLES</span></span>

### <span data-ttu-id="15072-108">Beispiel 1: Hinzufügen eines Profils</span><span class="sxs-lookup"><span data-stu-id="15072-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="15072-109">Mit diesem Befehl wird ein Container-Service-Agent-Pool Profil zum lokalen Containerdienst Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="15072-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="15072-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="15072-110">PARAMETERS</span></span>

### <span data-ttu-id="15072-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="15072-111">-ContainerService</span></span>
<span data-ttu-id="15072-112">Gibt das Containerdienst Objekt an, dem dieses Cmdlet ein Agenten Pool Profil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="15072-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="15072-113">Verwenden Sie zum Abrufen eines **ContainerService** -Objekts das Cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="15072-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15072-114">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="15072-114">-Count</span></span>
<span data-ttu-id="15072-115">Gibt die Anzahl der Agents an, die Container hosten.</span><span class="sxs-lookup"><span data-stu-id="15072-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="15072-116">Die zulässigen Werte für diesen Parameter sind: ganze Zahlen von 1 bis 100.</span><span class="sxs-lookup"><span data-stu-id="15072-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="15072-117">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="15072-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15072-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15072-118">-DefaultProfile</span></span>
<span data-ttu-id="15072-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15072-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15072-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="15072-120">-DnsPrefix</span></span>
<span data-ttu-id="15072-121">Gibt das DNS-Präfix an, mit dem dieses Cmdlet den vollqualifizierten Domänennamen für diesen Agent-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="15072-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15072-122">-Name</span><span class="sxs-lookup"><span data-stu-id="15072-122">-Name</span></span>
<span data-ttu-id="15072-123">Gibt den Namen des Agenten Pool Profils an.</span><span class="sxs-lookup"><span data-stu-id="15072-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="15072-124">Dieser Wert muss im Kontext der Abonnement-und Ressourcengruppe eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="15072-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15072-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="15072-125">-VmSize</span></span>
<span data-ttu-id="15072-126">Gibt die Größe der virtuellen Computer für die Agents an.</span><span class="sxs-lookup"><span data-stu-id="15072-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15072-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15072-127">-Confirm</span></span>
<span data-ttu-id="15072-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15072-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15072-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15072-129">-WhatIf</span></span>
<span data-ttu-id="15072-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15072-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15072-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15072-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15072-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15072-132">CommonParameters</span></span>
<span data-ttu-id="15072-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15072-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15072-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15072-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15072-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15072-135">INPUTS</span></span>

### <span data-ttu-id="15072-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="15072-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="15072-137">System. String</span><span class="sxs-lookup"><span data-stu-id="15072-137">System.String</span></span>

### <span data-ttu-id="15072-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="15072-138">System.Int32</span></span>

## <span data-ttu-id="15072-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15072-139">OUTPUTS</span></span>

### <span data-ttu-id="15072-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="15072-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="15072-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="15072-141">NOTES</span></span>

## <span data-ttu-id="15072-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15072-142">RELATED LINKS</span></span>

[<span data-ttu-id="15072-143">Neu – AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="15072-143">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="15072-144">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="15072-144">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
