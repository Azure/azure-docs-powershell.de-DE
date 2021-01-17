---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 23d14e88d7778402d69a6ea3248fa499e5e829cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473131"
---
# <span data-ttu-id="0650c-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0650c-101">Get-AzContainerService</span></span>

## <span data-ttu-id="0650c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0650c-102">SYNOPSIS</span></span>
<span data-ttu-id="0650c-103">Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="0650c-103">Gets a container service.</span></span>

## <span data-ttu-id="0650c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0650c-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0650c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0650c-105">DESCRIPTION</span></span>
<span data-ttu-id="0650c-106">Das **Cmdlet "Get-AzContainerService"** ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="0650c-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="0650c-107">Sie können die Eigenschaften eines Containerdiensts anzeigen, die den Zustand, die Anzahl der Master und Agents sowie den vollqualifizierten Domänennamen des Master- und Agentdiensts umfassen.</span><span class="sxs-lookup"><span data-stu-id="0650c-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="0650c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0650c-108">EXAMPLES</span></span>

### <span data-ttu-id="0650c-109">Beispiel 1: Erhalten eines Containerdiensts</span><span class="sxs-lookup"><span data-stu-id="0650c-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="0650c-110">Dieser Befehl ruft einen Containerdienst namens CSResourceGroup17 ab.</span><span class="sxs-lookup"><span data-stu-id="0650c-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="0650c-111">Beispiel 2: Alle Containerdienste erhalten</span><span class="sxs-lookup"><span data-stu-id="0650c-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="0650c-112">Dieser Befehl ruft alle Containerdienste im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0650c-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="0650c-113">Beispiel 3: Alle Containerdienste in der Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="0650c-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="0650c-114">Dieser Befehl ruft alle Containerdienste in ResourceGroup17 ab.</span><span class="sxs-lookup"><span data-stu-id="0650c-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="0650c-115">Beispiel 4: Alle Containerdienste mithilfe von Filter erhalten</span><span class="sxs-lookup"><span data-stu-id="0650c-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="0650c-116">Dieser Befehl ruft alle Containerdienste ab "CSResourceGroup1" ab.</span><span class="sxs-lookup"><span data-stu-id="0650c-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="0650c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0650c-117">PARAMETERS</span></span>

### <span data-ttu-id="0650c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0650c-118">-DefaultProfile</span></span>
<span data-ttu-id="0650c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0650c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0650c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0650c-120">-Name</span></span>
<span data-ttu-id="0650c-121">Gibt den Namen des Containerdiensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0650c-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0650c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0650c-122">-ResourceGroupName</span></span>
<span data-ttu-id="0650c-123">Gibt die Ressourcengruppe des Containerdiensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0650c-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0650c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0650c-124">CommonParameters</span></span>
<span data-ttu-id="0650c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0650c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0650c-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0650c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0650c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0650c-127">INPUTS</span></span>

### <span data-ttu-id="0650c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0650c-128">System.String</span></span>

## <span data-ttu-id="0650c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0650c-129">OUTPUTS</span></span>

### <span data-ttu-id="0650c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="0650c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="0650c-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0650c-131">NOTES</span></span>

## <span data-ttu-id="0650c-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0650c-132">RELATED LINKS</span></span>

[<span data-ttu-id="0650c-133">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0650c-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="0650c-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0650c-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="0650c-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0650c-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


