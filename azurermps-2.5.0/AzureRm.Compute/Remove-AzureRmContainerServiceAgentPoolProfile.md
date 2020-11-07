---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850088"
---
# <span data-ttu-id="2eaa9-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="2eaa9-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="2eaa9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2eaa9-102">SYNOPSIS</span></span>
<span data-ttu-id="2eaa9-103">Entfernt ein Profil eines Agenten Pools aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eaa9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eaa9-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eaa9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2eaa9-105">DESCRIPTION</span></span>
<span data-ttu-id="2eaa9-106">Das Cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** entfernt ein Agenten Pool Profil aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="2eaa9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2eaa9-107">EXAMPLES</span></span>

### <span data-ttu-id="2eaa9-108">Beispiel 1: Entfernen eines Profils aus einem Containerdienst</span><span class="sxs-lookup"><span data-stu-id="2eaa9-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="2eaa9-109">Der erste Befehl ruft einen Containerdienst mit dem Namen CSResourceGroup17 mithilfe des Get-AzureRmContainerService-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="2eaa9-110">Der Befehl speichert den Dienst in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="2eaa9-111">Der zweite Befehl entfernt das Profil mit dem Namen AgentPool01 aus dem Containerdienst in $Container.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="2eaa9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eaa9-112">PARAMETERS</span></span>

### <span data-ttu-id="2eaa9-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="2eaa9-113">-ContainerService</span></span>
<span data-ttu-id="2eaa9-114">Gibt das Containerdienst Objekt an, aus dem dieses Cmdlet ein Agenten Pool Profil entfernt.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="2eaa9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eaa9-115">-DefaultProfile</span></span>
<span data-ttu-id="2eaa9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eaa9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2eaa9-117">-Name</span></span>
<span data-ttu-id="2eaa9-118">Gibt den Namen des Agenten Pool Profils an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2eaa9-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2eaa9-119">-Confirm</span></span>
<span data-ttu-id="2eaa9-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eaa9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eaa9-121">-WhatIf</span></span>
<span data-ttu-id="2eaa9-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2eaa9-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eaa9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eaa9-124">CommonParameters</span></span>
<span data-ttu-id="2eaa9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eaa9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eaa9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eaa9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2eaa9-127">INPUTS</span></span>

### <span data-ttu-id="2eaa9-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="2eaa9-128">ContainerService</span></span>
<span data-ttu-id="2eaa9-129">Der Parameter "ContainerService" akzeptiert den Wert vom Typ "ContainerService" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="2eaa9-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2eaa9-130">OUTPUTS</span></span>

### <span data-ttu-id="2eaa9-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="2eaa9-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="2eaa9-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2eaa9-132">NOTES</span></span>

## <span data-ttu-id="2eaa9-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2eaa9-133">RELATED LINKS</span></span>

[<span data-ttu-id="2eaa9-134">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="2eaa9-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="2eaa9-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2eaa9-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


