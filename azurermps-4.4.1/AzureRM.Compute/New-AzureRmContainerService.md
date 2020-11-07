---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: d908f99e9a1eaa191b45ed08cdb69ebf40b21756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662278"
---
# <span data-ttu-id="4fdae-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4fdae-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="4fdae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4fdae-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdae-103">Erstellt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="4fdae-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fdae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fdae-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4fdae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fdae-105">DESCRIPTION</span></span>
<span data-ttu-id="4fdae-106">Das Cmdlet **New-AzureRmContainerService** erstellt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="4fdae-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="4fdae-107">Geben Sie ein Containerdienst Objekt an, das Sie mithilfe des New-AzureRmContainerServiceConfig-Cmdlets erstellen können.</span><span class="sxs-lookup"><span data-stu-id="4fdae-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="4fdae-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fdae-108">EXAMPLES</span></span>

### <span data-ttu-id="4fdae-109">Beispiel 1: Erstellen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="4fdae-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="4fdae-110">Der erste Befehl erstellt eine Ressourcengruppe mit dem Namen ResourceGroup17 an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="4fdae-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="4fdae-111">Weitere Informationen finden Sie im New-AzureRmResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fdae-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="4fdae-112">Der zweite Befehl erstellt einen Container und speichert ihn dann in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fdae-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4fdae-113">Weitere Informationen finden Sie im New-AzureRmContainerServiceConfig-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fdae-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="4fdae-114">Der endgültige Befehl erstellt einen Containerdienst für den Container, der in $Container gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4fdae-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="4fdae-115">Der Dienst hat den Namen csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="4fdae-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="4fdae-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fdae-116">PARAMETERS</span></span>

### <span data-ttu-id="4fdae-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="4fdae-117">-ContainerService</span></span>
<span data-ttu-id="4fdae-118">Gibt ein Containerdienst Objekt an, das die Eigenschaften für den neuen Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="4fdae-118">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="4fdae-119">Verwenden Sie das New-AzureRmContainerServiceConfig-Cmdlet, um ein **ContainerService** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fdae-119">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fdae-120">-DefaultProfile</span></span>
<span data-ttu-id="4fdae-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4fdae-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fdae-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4fdae-122">-Name</span></span>
<span data-ttu-id="4fdae-123">Gibt den Namen des vom Cmdlet erstellten Container Diensts an.</span><span class="sxs-lookup"><span data-stu-id="4fdae-123">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fdae-124">-ResourceGroupName</span></span>
<span data-ttu-id="4fdae-125">Gibt die Ressourcengruppe an, in der mit diesem Cmdlet der Containerdienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4fdae-125">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="4fdae-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4fdae-126">-Confirm</span></span>
<span data-ttu-id="4fdae-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4fdae-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdae-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fdae-128">-WhatIf</span></span>
<span data-ttu-id="4fdae-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fdae-129">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4fdae-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fdae-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdae-131">CommonParameters</span></span>
<span data-ttu-id="4fdae-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fdae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdae-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fdae-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdae-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4fdae-134">INPUTS</span></span>

## <span data-ttu-id="4fdae-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4fdae-135">OUTPUTS</span></span>

## <span data-ttu-id="4fdae-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="4fdae-136">NOTES</span></span>

## <span data-ttu-id="4fdae-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4fdae-137">RELATED LINKS</span></span>

[<span data-ttu-id="4fdae-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4fdae-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="4fdae-139">Neu – AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="4fdae-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="4fdae-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4fdae-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="4fdae-141">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4fdae-141">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


