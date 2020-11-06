---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 355938c64926d0c97d7e1393abd5c8a0d5ce20ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504197"
---
# <span data-ttu-id="825c2-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="825c2-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="825c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="825c2-102">SYNOPSIS</span></span>
<span data-ttu-id="825c2-103">Entfernt ein Profil eines Agenten Pools aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="825c2-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="825c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="825c2-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="825c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="825c2-105">DESCRIPTION</span></span>
<span data-ttu-id="825c2-106">Das Cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** entfernt ein Agenten Pool Profil aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="825c2-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="825c2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="825c2-107">EXAMPLES</span></span>

### <span data-ttu-id="825c2-108">Beispiel 1: Entfernen eines Profils aus einem Containerdienst</span><span class="sxs-lookup"><span data-stu-id="825c2-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="825c2-109">Der erste Befehl ruft einen Containerdienst mit dem Namen CSResourceGroup17 mithilfe des Get-AzureRmContainerService-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="825c2-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="825c2-110">Der Befehl speichert den Dienst in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="825c2-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="825c2-111">Der zweite Befehl entfernt das Profil mit dem Namen AgentPool01 aus dem Containerdienst in $Container.</span><span class="sxs-lookup"><span data-stu-id="825c2-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="825c2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="825c2-112">PARAMETERS</span></span>

### <span data-ttu-id="825c2-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="825c2-113">-ContainerService</span></span>
<span data-ttu-id="825c2-114">Gibt das Containerdienst Objekt an, aus dem dieses Cmdlet ein Agenten Pool Profil entfernt.</span><span class="sxs-lookup"><span data-stu-id="825c2-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="825c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825c2-115">-DefaultProfile</span></span>
<span data-ttu-id="825c2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="825c2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="825c2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="825c2-117">-Name</span></span>
<span data-ttu-id="825c2-118">Gibt den Namen des Agenten Pool Profils an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="825c2-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="825c2-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="825c2-119">-Confirm</span></span>
<span data-ttu-id="825c2-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="825c2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="825c2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="825c2-121">-WhatIf</span></span>
<span data-ttu-id="825c2-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="825c2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="825c2-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="825c2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="825c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825c2-124">CommonParameters</span></span>
<span data-ttu-id="825c2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="825c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825c2-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="825c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825c2-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="825c2-127">INPUTS</span></span>

## <span data-ttu-id="825c2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="825c2-128">OUTPUTS</span></span>

## <span data-ttu-id="825c2-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="825c2-129">NOTES</span></span>

## <span data-ttu-id="825c2-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="825c2-130">RELATED LINKS</span></span>

[<span data-ttu-id="825c2-131">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="825c2-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="825c2-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="825c2-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


