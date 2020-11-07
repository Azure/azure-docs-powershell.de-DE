---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: a89494b155755cf716f39275debcfb7477071da2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849788"
---
# <span data-ttu-id="b7a5a-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b7a5a-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="b7a5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a5a-103">Fügt ein Pool Profil für Containerdienst-Agents hinzu.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7a5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7a5a-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7a5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a5a-106">Mit dem Cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** wird ein Containerdienst-Agent-Pool Profil zu einem lokalen Containerdienst Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="b7a5a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7a5a-107">EXAMPLES</span></span>

### <span data-ttu-id="b7a5a-108">Beispiel 1: Hinzufügen eines Profils</span><span class="sxs-lookup"><span data-stu-id="b7a5a-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="b7a5a-109">Mit diesem Befehl wird ein Container-Service-Agent-Pool Profil zum lokalen Containerdienst Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="b7a5a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7a5a-110">PARAMETERS</span></span>

### <span data-ttu-id="b7a5a-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="b7a5a-111">-ContainerService</span></span>
<span data-ttu-id="b7a5a-112">Gibt das Containerdienst Objekt an, dem dieses Cmdlet ein Agenten Pool Profil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="b7a5a-113">Verwenden Sie zum Abrufen eines **ContainerService** -Objekts das Cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="b7a5a-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5a-114">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="b7a5a-114">-Count</span></span>
<span data-ttu-id="b7a5a-115">Gibt die Anzahl der Agents an, die Container hosten.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="b7a5a-116">Die zulässigen Werte für diesen Parameter sind: ganze Zahlen von 1 bis 100.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="b7a5a-117">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-117">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a5a-118">-DefaultProfile</span></span>
<span data-ttu-id="b7a5a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5a-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="b7a5a-120">-DnsPrefix</span></span>
<span data-ttu-id="b7a5a-121">Gibt das DNS-Präfix an, mit dem dieses Cmdlet den vollqualifizierten Domänennamen für diesen Agent-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b7a5a-122">-Name</span></span>
<span data-ttu-id="b7a5a-123">Gibt den Namen des Agenten Pool Profils an.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="b7a5a-124">Dieser Wert muss im Kontext der Abonnement-und Ressourcengruppe eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5a-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="b7a5a-125">-VmSize</span></span>
<span data-ttu-id="b7a5a-126">Gibt die Größe der virtuellen Computer für die Agents an.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7a5a-127">-Confirm</span></span>
<span data-ttu-id="b7a5a-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7a5a-129">-WhatIf</span></span>
<span data-ttu-id="b7a5a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7a5a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a5a-132">CommonParameters</span></span>
<span data-ttu-id="b7a5a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a5a-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7a5a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a5a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7a5a-135">INPUTS</span></span>

### <span data-ttu-id="b7a5a-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="b7a5a-136">ContainerService</span></span>
<span data-ttu-id="b7a5a-137">Der Parameter "ContainerService" akzeptiert den Wert vom Typ "ContainerService" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b7a5a-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="b7a5a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7a5a-138">OUTPUTS</span></span>

### <span data-ttu-id="b7a5a-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="b7a5a-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="b7a5a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7a5a-140">NOTES</span></span>

## <span data-ttu-id="b7a5a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7a5a-141">RELATED LINKS</span></span>

[<span data-ttu-id="b7a5a-142">Neu – AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="b7a5a-142">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="b7a5a-143">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b7a5a-143">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
