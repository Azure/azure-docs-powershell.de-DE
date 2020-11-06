---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: 62acfacbafb50f85673b37e802b9d0b0eb4bf66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476905"
---
# <span data-ttu-id="bef07-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="bef07-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="bef07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bef07-102">SYNOPSIS</span></span>
<span data-ttu-id="bef07-103">Aktualisiert den Zustand eines Container Diensts.</span><span class="sxs-lookup"><span data-stu-id="bef07-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bef07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bef07-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bef07-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bef07-105">DESCRIPTION</span></span>
<span data-ttu-id="bef07-106">Das Cmdlet **Update-AzureRmContainerService** aktualisiert den Zustand eines Container Diensts so, dass er einer lokalen Instanz des Diensts entspricht.</span><span class="sxs-lookup"><span data-stu-id="bef07-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="bef07-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bef07-107">EXAMPLES</span></span>

### <span data-ttu-id="bef07-108">Beispiel 1: Aktualisieren eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="bef07-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="bef07-109">Dieser Befehl ruft den Containerdienst mit dem Namen CSResourceGroup17 mithilfe des Get-AzureRmContainerService-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="bef07-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="bef07-110">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das Remove-AzureRmContainerServiceAgentPoolProfile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef07-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="bef07-111">**Remove-AzureRmContainerServiceAgentPoolProfile** entfernt das Profil mit dem Namen AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="bef07-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="bef07-112">Der Befehl übergibt das Ergebnis an das Add-AzureRmContainerServiceAgentPoolProfile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef07-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="bef07-113">**Add-AzureRmContainerServiceAgentPoolProfile** fügt ein Profil mit dem Namen AgentPool01 hinzu und weist die angegebenen Eigenschaften auf.</span><span class="sxs-lookup"><span data-stu-id="bef07-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="bef07-114">Der Befehl übergibt das Ergebnis an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef07-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="bef07-115">Das aktuelle Cmdlet aktualisiert den Containerdienst so, dass die Änderungen, die in diesem Befehl vorgenommen wurden, wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bef07-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="bef07-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bef07-116">PARAMETERS</span></span>

### <span data-ttu-id="bef07-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="bef07-117">-ContainerService</span></span>
<span data-ttu-id="bef07-118">Gibt ein lokales **ContainerService** -Objekt an, das Änderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="bef07-118">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bef07-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bef07-119">-Name</span></span>
<span data-ttu-id="bef07-120">Gibt den Namen des Container Diensts an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="bef07-120">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef07-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef07-121">-ResourceGroupName</span></span>
<span data-ttu-id="bef07-122">Gibt die Ressourcengruppe des Container Diensts an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="bef07-122">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="bef07-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bef07-123">-Confirm</span></span>
<span data-ttu-id="bef07-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bef07-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef07-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bef07-125">-WhatIf</span></span>
<span data-ttu-id="bef07-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bef07-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bef07-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bef07-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef07-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef07-128">CommonParameters</span></span>
<span data-ttu-id="bef07-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef07-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef07-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef07-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef07-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bef07-131">INPUTS</span></span>

### <span data-ttu-id="bef07-132">Keine</span><span class="sxs-lookup"><span data-stu-id="bef07-132">None</span></span>
<span data-ttu-id="bef07-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bef07-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bef07-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bef07-134">OUTPUTS</span></span>

## <span data-ttu-id="bef07-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="bef07-135">NOTES</span></span>

## <span data-ttu-id="bef07-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bef07-136">RELATED LINKS</span></span>

[<span data-ttu-id="bef07-137">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="bef07-137">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="bef07-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="bef07-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="bef07-139">Neu – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="bef07-139">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="bef07-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="bef07-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="bef07-141">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="bef07-141">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


