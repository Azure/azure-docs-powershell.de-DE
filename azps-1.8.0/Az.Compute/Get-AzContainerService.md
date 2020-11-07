---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 9d8afa31d296e62c75b869bd93e6f96aadf82328
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661567"
---
# <span data-ttu-id="a324d-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a324d-101">Get-AzContainerService</span></span>

## <span data-ttu-id="a324d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a324d-102">SYNOPSIS</span></span>
<span data-ttu-id="a324d-103">Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="a324d-103">Gets a container service.</span></span>

## <span data-ttu-id="a324d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a324d-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a324d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a324d-105">DESCRIPTION</span></span>
<span data-ttu-id="a324d-106">Das Cmdlet " **Get-AzContainerService** " Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="a324d-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="a324d-107">Sie können die Eigenschaften eines Container Diensts anzeigen, der den Status, die Anzahl der Master und Agents sowie den vollqualifizierten Domänennamenmaster und Agent umfasst.</span><span class="sxs-lookup"><span data-stu-id="a324d-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="a324d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a324d-108">EXAMPLES</span></span>

### <span data-ttu-id="a324d-109">Beispiel 1: Abrufen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="a324d-109">Example 1: Get a container service</span></span>
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

<span data-ttu-id="a324d-110">Dieser Befehl ruft einen Containerdienst mit dem Namen CSResourceGroup17 ab.</span><span class="sxs-lookup"><span data-stu-id="a324d-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="a324d-111">Beispiel 2: Abrufen aller Container Dienste</span><span class="sxs-lookup"><span data-stu-id="a324d-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="a324d-112">Dieser Befehl ruft alle Container Dienste im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a324d-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="a324d-113">Beispiel 3: Abrufen aller Container Dienste in der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a324d-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="a324d-114">Dieser Befehl ruft alle Container Dienste in ResourceGroup17 ab.</span><span class="sxs-lookup"><span data-stu-id="a324d-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="a324d-115">Beispiel 4: Abrufen aller Container Dienste mithilfe von Filter</span><span class="sxs-lookup"><span data-stu-id="a324d-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="a324d-116">Dieser Befehl ruft alle Container Dienste ab, die mit "CSResourceGroup1" beginnen.</span><span class="sxs-lookup"><span data-stu-id="a324d-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="a324d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a324d-117">PARAMETERS</span></span>

### <span data-ttu-id="a324d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a324d-118">-DefaultProfile</span></span>
<span data-ttu-id="a324d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a324d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a324d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a324d-120">-Name</span></span>
<span data-ttu-id="a324d-121">Gibt den Namen des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a324d-121">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a324d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a324d-122">-ResourceGroupName</span></span>
<span data-ttu-id="a324d-123">Gibt die Ressourcengruppe des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a324d-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a324d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a324d-124">CommonParameters</span></span>
<span data-ttu-id="a324d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a324d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a324d-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a324d-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a324d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a324d-127">INPUTS</span></span>

### <span data-ttu-id="a324d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a324d-128">System.String</span></span>

## <span data-ttu-id="a324d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a324d-129">OUTPUTS</span></span>

### <span data-ttu-id="a324d-130">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="a324d-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="a324d-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a324d-131">NOTES</span></span>

## <span data-ttu-id="a324d-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a324d-132">RELATED LINKS</span></span>

[<span data-ttu-id="a324d-133">Neu – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a324d-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="a324d-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a324d-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="a324d-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a324d-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


