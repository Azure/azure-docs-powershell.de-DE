---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: cc9b536517a70fd7c004be6fcac300afa0a4760b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652175"
---
# <span data-ttu-id="895be-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="895be-101">Get-AzHost</span></span>

## <span data-ttu-id="895be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="895be-102">SYNOPSIS</span></span>
<span data-ttu-id="895be-103">Abrufen oder Auflisten von Hosts</span><span class="sxs-lookup"><span data-stu-id="895be-103">Get or list hosts.</span></span>

## <span data-ttu-id="895be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="895be-104">SYNTAX</span></span>

### <span data-ttu-id="895be-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="895be-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="895be-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="895be-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="895be-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="895be-107">DESCRIPTION</span></span>
<span data-ttu-id="895be-108">Dieses Cmdlet erhält einen Host in einer Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="895be-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="895be-109">Dieses Cmdlet listet auch alle Hosts in einer Hostgruppe auf, wenn kein Hostname angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="895be-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="895be-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="895be-110">EXAMPLES</span></span>

### <span data-ttu-id="895be-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="895be-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="895be-112">Dieser Befehl gibt einen Host zurück.</span><span class="sxs-lookup"><span data-stu-id="895be-112">This command returns a host.</span></span>

### <span data-ttu-id="895be-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="895be-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="895be-114">Dieser Befehl gibt die Instanzen Ansicht eines Hosts zurück.</span><span class="sxs-lookup"><span data-stu-id="895be-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="895be-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="895be-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="895be-116">Dieser Befehl gibt alle Hosts in der angegebenen Hostgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="895be-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="895be-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="895be-117">PARAMETERS</span></span>

### <span data-ttu-id="895be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="895be-118">-DefaultProfile</span></span>
<span data-ttu-id="895be-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="895be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895be-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="895be-120">-HostGroupName</span></span>
<span data-ttu-id="895be-121">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="895be-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="895be-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="895be-122">-InstanceView</span></span>
<span data-ttu-id="895be-123">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des Hosts abruft.</span><span class="sxs-lookup"><span data-stu-id="895be-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895be-124">-Name</span><span class="sxs-lookup"><span data-stu-id="895be-124">-Name</span></span>
<span data-ttu-id="895be-125">Der Name des Hosts.</span><span class="sxs-lookup"><span data-stu-id="895be-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="895be-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="895be-126">-ResourceGroupName</span></span>
<span data-ttu-id="895be-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="895be-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="895be-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="895be-128">-ResourceId</span></span>
<span data-ttu-id="895be-129">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="895be-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="895be-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="895be-130">CommonParameters</span></span>
<span data-ttu-id="895be-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="895be-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="895be-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="895be-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="895be-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="895be-133">INPUTS</span></span>

### <span data-ttu-id="895be-134">System. String</span><span class="sxs-lookup"><span data-stu-id="895be-134">System.String</span></span>

## <span data-ttu-id="895be-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="895be-135">OUTPUTS</span></span>

### <span data-ttu-id="895be-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="895be-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="895be-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="895be-137">NOTES</span></span>

## <span data-ttu-id="895be-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="895be-138">RELATED LINKS</span></span>
