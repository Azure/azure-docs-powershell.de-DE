---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178946"
---
# <span data-ttu-id="115d1-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="115d1-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="115d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="115d1-102">SYNOPSIS</span></span>
<span data-ttu-id="115d1-103">Der Vorgang, um die Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="115d1-103">The operation to get the extension.</span></span>

## <span data-ttu-id="115d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="115d1-104">SYNTAX</span></span>

### <span data-ttu-id="115d1-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="115d1-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="115d1-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="115d1-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="115d1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="115d1-107">DESCRIPTION</span></span>
<span data-ttu-id="115d1-108">Der Vorgang, um die Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="115d1-108">The operation to get the extension.</span></span>

## <span data-ttu-id="115d1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="115d1-109">EXAMPLES</span></span>

### <span data-ttu-id="115d1-110">Beispiel 1: Auflisten aller Erweiterungen für einen Computer</span><span class="sxs-lookup"><span data-stu-id="115d1-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="115d1-111">Listet alle Erweiterungen für einen bestimmten Computer auf.</span><span class="sxs-lookup"><span data-stu-id="115d1-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="115d1-112">Beispiel 2: Abrufen einer bestimmten Erweiterung auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="115d1-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="115d1-113">Ruft eine bestimmte Erweiterung auf einem Computer ab.</span><span class="sxs-lookup"><span data-stu-id="115d1-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="115d1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="115d1-114">PARAMETERS</span></span>

### <span data-ttu-id="115d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115d1-115">-DefaultProfile</span></span>
<span data-ttu-id="115d1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="115d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="115d1-117">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="115d1-117">-Expand</span></span>
<span data-ttu-id="115d1-118">Der Expand-Ausdruck, der auf den Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="115d1-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115d1-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="115d1-119">-MachineName</span></span>
<span data-ttu-id="115d1-120">Der Name des Computers, der die Erweiterung enthält.</span><span class="sxs-lookup"><span data-stu-id="115d1-120">The name of the machine containing the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115d1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="115d1-121">-Name</span></span>
<span data-ttu-id="115d1-122">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="115d1-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="115d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="115d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="115d1-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="115d1-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115d1-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="115d1-125">-SubscriptionId</span></span>
<span data-ttu-id="115d1-126">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="115d1-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="115d1-127">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="115d1-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="115d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115d1-128">CommonParameters</span></span>
<span data-ttu-id="115d1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="115d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115d1-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="115d1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115d1-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="115d1-131">INPUTS</span></span>

## <span data-ttu-id="115d1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="115d1-132">OUTPUTS</span></span>

### <span data-ttu-id="115d1-133">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="115d1-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="115d1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="115d1-134">NOTES</span></span>

<span data-ttu-id="115d1-135">Aliase</span><span class="sxs-lookup"><span data-stu-id="115d1-135">ALIASES</span></span>

## <span data-ttu-id="115d1-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="115d1-136">RELATED LINKS</span></span>

