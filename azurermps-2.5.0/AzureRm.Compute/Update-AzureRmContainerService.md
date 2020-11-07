---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 9a199a0aa0e31cf8bc57585d4825a33e10b5bfc1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850871"
---
# <span data-ttu-id="b5021-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b5021-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="b5021-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5021-102">SYNOPSIS</span></span>
<span data-ttu-id="b5021-103">Aktualisiert den Zustand eines Container Diensts.</span><span class="sxs-lookup"><span data-stu-id="b5021-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5021-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5021-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5021-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5021-105">DESCRIPTION</span></span>
<span data-ttu-id="b5021-106">Das Cmdlet **Update-AzureRmContainerService** aktualisiert den Zustand eines Container Diensts so, dass er einer lokalen Instanz des Diensts entspricht.</span><span class="sxs-lookup"><span data-stu-id="b5021-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="b5021-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5021-107">EXAMPLES</span></span>

### <span data-ttu-id="b5021-108">Beispiel 1: Aktualisieren eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="b5021-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="b5021-109">Dieser Befehl ruft den Containerdienst mit dem Namen CSResourceGroup17 mithilfe des Get-AzureRmContainerService-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="b5021-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="b5021-110">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das Remove-AzureRmContainerServiceAgentPoolProfile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5021-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="b5021-111">**Remove-AzureRmContainerServiceAgentPoolProfile** entfernt das Profil mit dem Namen AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="b5021-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="b5021-112">Der Befehl übergibt das Ergebnis an das Add-AzureRmContainerServiceAgentPoolProfile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5021-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="b5021-113">**Add-AzureRmContainerServiceAgentPoolProfile** fügt ein Profil mit dem Namen AgentPool01 hinzu und weist die angegebenen Eigenschaften auf.</span><span class="sxs-lookup"><span data-stu-id="b5021-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="b5021-114">Der Befehl übergibt das Ergebnis an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5021-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="b5021-115">Das aktuelle Cmdlet aktualisiert den Containerdienst so, dass die Änderungen, die in diesem Befehl vorgenommen wurden, wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b5021-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="b5021-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5021-116">PARAMETERS</span></span>

### <span data-ttu-id="b5021-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5021-117">-AsJob</span></span>
<span data-ttu-id="b5021-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b5021-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5021-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="b5021-119">-ContainerService</span></span>
<span data-ttu-id="b5021-120">Gibt ein lokales **ContainerService** -Objekt an, das Änderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="b5021-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5021-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5021-121">-DefaultProfile</span></span>
<span data-ttu-id="b5021-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5021-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5021-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b5021-123">-Name</span></span>
<span data-ttu-id="b5021-124">Gibt den Namen des Container Diensts an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b5021-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b5021-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5021-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5021-126">Gibt die Ressourcengruppe des Container Diensts an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b5021-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b5021-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b5021-127">-Confirm</span></span>
<span data-ttu-id="b5021-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5021-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5021-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5021-129">-WhatIf</span></span>
<span data-ttu-id="b5021-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5021-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b5021-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5021-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5021-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5021-132">CommonParameters</span></span>
<span data-ttu-id="b5021-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5021-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5021-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5021-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5021-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5021-135">INPUTS</span></span>

### <span data-ttu-id="b5021-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="b5021-136">ContainerService</span></span>
<span data-ttu-id="b5021-137">Der Parameter "ContainerService" akzeptiert den Wert vom Typ "ContainerService" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5021-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="b5021-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5021-138">OUTPUTS</span></span>

### <span data-ttu-id="b5021-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="b5021-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="b5021-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5021-140">NOTES</span></span>

## <span data-ttu-id="b5021-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5021-141">RELATED LINKS</span></span>

[<span data-ttu-id="b5021-142">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b5021-142">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="b5021-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b5021-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="b5021-144">Neu – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b5021-144">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="b5021-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b5021-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="b5021-146">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b5021-146">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


