---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: cfcb3c7657bc0ff99646c3ef21eb5cceb592fe2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662371"
---
# <span data-ttu-id="7c250-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7c250-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="7c250-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c250-102">SYNOPSIS</span></span>
<span data-ttu-id="7c250-103">Entfernt ein Profil eines Agenten Pools aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="7c250-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c250-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c250-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [-Name] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c250-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c250-105">DESCRIPTION</span></span>
<span data-ttu-id="7c250-106">Das Cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** entfernt ein Agenten Pool Profil aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="7c250-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="7c250-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c250-107">EXAMPLES</span></span>

### <span data-ttu-id="7c250-108">Beispiel 1: Entfernen eines Profils aus einem Containerdienst</span><span class="sxs-lookup"><span data-stu-id="7c250-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="7c250-109">Der erste Befehl ruft einen Containerdienst mit dem Namen CSResourceGroup17 mithilfe des Get-AzureRmContainerService-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="7c250-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="7c250-110">Der Befehl speichert den Dienst in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7c250-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="7c250-111">Der zweite Befehl entfernt das Profil mit dem Namen AgentPool01 aus dem Containerdienst in $Container.</span><span class="sxs-lookup"><span data-stu-id="7c250-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="7c250-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c250-112">PARAMETERS</span></span>

### <span data-ttu-id="7c250-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="7c250-113">-ContainerService</span></span>
<span data-ttu-id="7c250-114">Gibt das Containerdienst Objekt an, aus dem dieses Cmdlet ein Agenten Pool Profil entfernt.</span><span class="sxs-lookup"><span data-stu-id="7c250-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="7c250-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7c250-115">-Name</span></span>
<span data-ttu-id="7c250-116">Gibt den Namen des Agenten Pool Profils an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7c250-116">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c250-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c250-117">-Confirm</span></span>
<span data-ttu-id="7c250-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c250-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c250-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c250-119">-WhatIf</span></span>
<span data-ttu-id="7c250-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c250-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c250-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c250-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c250-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c250-122">CommonParameters</span></span>
<span data-ttu-id="7c250-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c250-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c250-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c250-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c250-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c250-125">INPUTS</span></span>

### <span data-ttu-id="7c250-126">Keine</span><span class="sxs-lookup"><span data-stu-id="7c250-126">None</span></span>
<span data-ttu-id="7c250-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7c250-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c250-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c250-128">OUTPUTS</span></span>

## <span data-ttu-id="7c250-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c250-129">NOTES</span></span>

## <span data-ttu-id="7c250-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c250-130">RELATED LINKS</span></span>

[<span data-ttu-id="7c250-131">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7c250-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="7c250-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="7c250-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


