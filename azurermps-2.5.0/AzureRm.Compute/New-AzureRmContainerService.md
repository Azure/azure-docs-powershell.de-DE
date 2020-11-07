---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 6d1a891dbef40a6556e3a8f2ca122f2c3b46cb28
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848531"
---
# <span data-ttu-id="92528-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="92528-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="92528-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92528-102">SYNOPSIS</span></span>
<span data-ttu-id="92528-103">Erstellt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="92528-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92528-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92528-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92528-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92528-105">DESCRIPTION</span></span>
<span data-ttu-id="92528-106">Das Cmdlet **New-AzureRmContainerService** erstellt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="92528-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="92528-107">Geben Sie ein Containerdienst Objekt an, das Sie mithilfe des New-AzureRmContainerServiceConfig-Cmdlets erstellen können.</span><span class="sxs-lookup"><span data-stu-id="92528-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="92528-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92528-108">EXAMPLES</span></span>

### <span data-ttu-id="92528-109">Beispiel 1: Erstellen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="92528-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="92528-110">Der erste Befehl erstellt eine Ressourcengruppe mit dem Namen ResourceGroup17 an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="92528-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="92528-111">Weitere Informationen finden Sie im New-AzureRmResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92528-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="92528-112">Der zweite Befehl erstellt einen Container und speichert ihn dann in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="92528-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="92528-113">Weitere Informationen finden Sie im New-AzureRmContainerServiceConfig-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92528-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="92528-114">Der endgültige Befehl erstellt einen Containerdienst für den Container, der in $Container gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="92528-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="92528-115">Der Dienst hat den Namen csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="92528-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="92528-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="92528-116">PARAMETERS</span></span>

### <span data-ttu-id="92528-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92528-117">-AsJob</span></span>
<span data-ttu-id="92528-118">RRun-Cmdlet im Hintergrund, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="92528-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="92528-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="92528-119">-ContainerService</span></span>
<span data-ttu-id="92528-120">Gibt ein Containerdienst Objekt an, das die Eigenschaften für den neuen Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="92528-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="92528-121">Verwenden Sie das New-AzureRmContainerServiceConfig-Cmdlet, um ein **ContainerService** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="92528-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="92528-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92528-122">-DefaultProfile</span></span>
<span data-ttu-id="92528-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92528-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92528-124">-Name</span><span class="sxs-lookup"><span data-stu-id="92528-124">-Name</span></span>
<span data-ttu-id="92528-125">Gibt den Namen des vom Cmdlet erstellten Container Diensts an.</span><span class="sxs-lookup"><span data-stu-id="92528-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="92528-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92528-126">-ResourceGroupName</span></span>
<span data-ttu-id="92528-127">Gibt die Ressourcengruppe an, in der mit diesem Cmdlet der Containerdienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="92528-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="92528-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92528-128">-Confirm</span></span>
<span data-ttu-id="92528-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92528-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92528-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92528-130">-WhatIf</span></span>
<span data-ttu-id="92528-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92528-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="92528-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92528-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92528-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92528-133">CommonParameters</span></span>
<span data-ttu-id="92528-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92528-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92528-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92528-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92528-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92528-136">INPUTS</span></span>

### <span data-ttu-id="92528-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="92528-137">ContainerService</span></span>
<span data-ttu-id="92528-138">Der Parameter "ContainerService" akzeptiert den Wert vom Typ "ContainerService" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="92528-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="92528-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92528-139">OUTPUTS</span></span>

### <span data-ttu-id="92528-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="92528-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="92528-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="92528-141">NOTES</span></span>

## <span data-ttu-id="92528-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92528-142">RELATED LINKS</span></span>

[<span data-ttu-id="92528-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="92528-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="92528-144">Neu – AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="92528-144">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="92528-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="92528-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="92528-146">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="92528-146">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


