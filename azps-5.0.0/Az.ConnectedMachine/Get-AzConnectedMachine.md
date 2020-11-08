---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178947"
---
# <span data-ttu-id="70d1a-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="70d1a-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="70d1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="70d1a-103">Ruft Informationen zur Modellansicht oder zur Instanzen Ansicht eines Hybrid Computers ab.</span><span class="sxs-lookup"><span data-stu-id="70d1a-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="70d1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70d1a-104">SYNTAX</span></span>

### <span data-ttu-id="70d1a-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="70d1a-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70d1a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="70d1a-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70d1a-107">Liste</span><span class="sxs-lookup"><span data-stu-id="70d1a-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="70d1a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70d1a-108">DESCRIPTION</span></span>
<span data-ttu-id="70d1a-109">Ruft Informationen zur Modellansicht oder zur Instanzen Ansicht eines Hybrid Computers ab.</span><span class="sxs-lookup"><span data-stu-id="70d1a-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="70d1a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70d1a-110">EXAMPLES</span></span>

### <span data-ttu-id="70d1a-111">Beispiel 1: Auflisten aller verbundenen Computer in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="70d1a-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="70d1a-112">Listet alle verbundenen Computer in einem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="70d1a-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="70d1a-113">Wenn das Abonnement nicht angegeben ist, wird das Abonnement aus dem aktuellen Azure PowerShell-Kontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="70d1a-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="70d1a-114">Beispiel 2: Auflisten aller verbundenen Computer in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="70d1a-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="70d1a-115">Auflisten aller verbundenen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="70d1a-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="70d1a-116">Beispiel 3: Abrufen eines verbundenen Computers in einer Ressourcengruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="70d1a-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="70d1a-117">Abrufen eines verbundenen Computers in einer Ressourcengruppe nach Namen.</span><span class="sxs-lookup"><span data-stu-id="70d1a-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="70d1a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="70d1a-118">PARAMETERS</span></span>

### <span data-ttu-id="70d1a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d1a-119">-DefaultProfile</span></span>
<span data-ttu-id="70d1a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70d1a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d1a-121">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="70d1a-121">-Expand</span></span>
<span data-ttu-id="70d1a-122">Der Expand-Ausdruck, der auf den Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70d1a-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d1a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="70d1a-123">-Name</span></span>
<span data-ttu-id="70d1a-124">Der Name der hybridmaschine.</span><span class="sxs-lookup"><span data-stu-id="70d1a-124">The name of the hybrid machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d1a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d1a-125">-ResourceGroupName</span></span>
<span data-ttu-id="70d1a-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="70d1a-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d1a-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="70d1a-127">-SubscriptionId</span></span>
<span data-ttu-id="70d1a-128">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="70d1a-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="70d1a-129">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="70d1a-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d1a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d1a-130">CommonParameters</span></span>
<span data-ttu-id="70d1a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d1a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d1a-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70d1a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d1a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70d1a-133">INPUTS</span></span>

## <span data-ttu-id="70d1a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70d1a-134">OUTPUTS</span></span>

### <span data-ttu-id="70d1a-135">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachine</span><span class="sxs-lookup"><span data-stu-id="70d1a-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="70d1a-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="70d1a-136">NOTES</span></span>

<span data-ttu-id="70d1a-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="70d1a-137">ALIASES</span></span>

## <span data-ttu-id="70d1a-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70d1a-138">RELATED LINKS</span></span>

