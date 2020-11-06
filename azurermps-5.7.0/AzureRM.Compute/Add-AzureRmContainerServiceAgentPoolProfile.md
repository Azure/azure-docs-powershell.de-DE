---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b3df5b930cd7b30af8fef35735eea56eab7a5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499049"
---
# <span data-ttu-id="154f1-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="154f1-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="154f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="154f1-102">SYNOPSIS</span></span>
<span data-ttu-id="154f1-103">Fügt ein Pool Profil für Containerdienst-Agents hinzu.</span><span class="sxs-lookup"><span data-stu-id="154f1-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="154f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="154f1-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="154f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="154f1-105">DESCRIPTION</span></span>
<span data-ttu-id="154f1-106">Mit dem Cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** wird ein Containerdienst-Agent-Pool Profil zu einem lokalen Containerdienst Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="154f1-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="154f1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="154f1-107">EXAMPLES</span></span>

### <span data-ttu-id="154f1-108">Beispiel 1: Hinzufügen eines Profils</span><span class="sxs-lookup"><span data-stu-id="154f1-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="154f1-109">Mit diesem Befehl wird ein Container-Service-Agent-Pool Profil zum lokalen Containerdienst Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="154f1-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="154f1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="154f1-110">PARAMETERS</span></span>

### <span data-ttu-id="154f1-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="154f1-111">-ContainerService</span></span>
<span data-ttu-id="154f1-112">Gibt das Containerdienst Objekt an, dem dieses Cmdlet ein Agenten Pool Profil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="154f1-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="154f1-113">Verwenden Sie zum Abrufen eines **ContainerService** -Objekts das Cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="154f1-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="154f1-114">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="154f1-114">-Count</span></span>
<span data-ttu-id="154f1-115">Gibt die Anzahl der Agents an, die Container hosten.</span><span class="sxs-lookup"><span data-stu-id="154f1-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="154f1-116">Die zulässigen Werte für diesen Parameter sind: ganze Zahlen von 1 bis 100.</span><span class="sxs-lookup"><span data-stu-id="154f1-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="154f1-117">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="154f1-117">The default value is 1.</span></span>

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

### <span data-ttu-id="154f1-118">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="154f1-118">-DnsPrefix</span></span>
<span data-ttu-id="154f1-119">Gibt das DNS-Präfix an, mit dem dieses Cmdlet den vollqualifizierten Domänennamen für diesen Agent-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="154f1-119">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="154f1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="154f1-120">-Name</span></span>
<span data-ttu-id="154f1-121">Gibt den Namen des Agenten Pool Profils an.</span><span class="sxs-lookup"><span data-stu-id="154f1-121">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="154f1-122">Dieser Wert muss im Kontext der Abonnement-und Ressourcengruppe eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="154f1-122">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="154f1-123">-VmSize</span><span class="sxs-lookup"><span data-stu-id="154f1-123">-VmSize</span></span>
<span data-ttu-id="154f1-124">Gibt die Größe der virtuellen Computer für die Agents an.</span><span class="sxs-lookup"><span data-stu-id="154f1-124">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="154f1-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="154f1-125">-Confirm</span></span>
<span data-ttu-id="154f1-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="154f1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="154f1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="154f1-127">-WhatIf</span></span>
<span data-ttu-id="154f1-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="154f1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="154f1-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="154f1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="154f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154f1-130">CommonParameters</span></span>
<span data-ttu-id="154f1-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="154f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154f1-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="154f1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154f1-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="154f1-133">INPUTS</span></span>

### <span data-ttu-id="154f1-134">Keine</span><span class="sxs-lookup"><span data-stu-id="154f1-134">None</span></span>
<span data-ttu-id="154f1-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="154f1-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="154f1-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="154f1-136">OUTPUTS</span></span>

## <span data-ttu-id="154f1-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="154f1-137">NOTES</span></span>

## <span data-ttu-id="154f1-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="154f1-138">RELATED LINKS</span></span>

[<span data-ttu-id="154f1-139">Neu – AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="154f1-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="154f1-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="154f1-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
