---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290027"
---
# <span data-ttu-id="0c881-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="0c881-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="0c881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c881-102">SYNOPSIS</span></span>
<span data-ttu-id="0c881-103">API zum Registrieren eines neuen Computers und damit zum Erstellen einer nachverfolgten Ressource in ARM</span><span class="sxs-lookup"><span data-stu-id="0c881-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="0c881-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c881-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="0c881-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c881-105">DESCRIPTION</span></span>
<span data-ttu-id="0c881-106">API zum Registrieren eines neuen Computers und damit zum Erstellen einer nachverfolgten Ressource in ARM</span><span class="sxs-lookup"><span data-stu-id="0c881-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="0c881-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c881-107">EXAMPLES</span></span>

### <span data-ttu-id="0c881-108">Beispiel 1: Onboarding des Computers, den Sie als verbundenen Computer haben</span><span class="sxs-lookup"><span data-stu-id="0c881-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="0c881-109">Onboards the machine you're on as a connected machine.</span><span class="sxs-lookup"><span data-stu-id="0c881-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="0c881-110">Beispiel 2: Onboarding eines Remotecomputers als verbundenes Gerät</span><span class="sxs-lookup"><span data-stu-id="0c881-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="0c881-111">Onboards a remote machine as a connected device using PowerShell remoting.</span><span class="sxs-lookup"><span data-stu-id="0c881-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="0c881-112">Hinweis: Derzeit wird nur Windows als Ziel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0c881-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="0c881-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c881-113">PARAMETERS</span></span>

### <span data-ttu-id="0c881-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c881-114">-DefaultProfile</span></span>
<span data-ttu-id="0c881-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c881-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c881-116">-Location</span><span class="sxs-lookup"><span data-stu-id="0c881-116">-Location</span></span>
<span data-ttu-id="0c881-117">Der Speicherort für die erstellte "ConnectedMachine".</span><span class="sxs-lookup"><span data-stu-id="0c881-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c881-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0c881-118">-Name</span></span>
<span data-ttu-id="0c881-119">Der Name, der für diesen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c881-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="0c881-120">Der Hostname wird standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c881-120">The hostname is used by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c881-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="0c881-121">-Proxy</span></span>
<span data-ttu-id="0c881-122">Der URI für den zu verwendende Proxyserver</span><span class="sxs-lookup"><span data-stu-id="0c881-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c881-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="0c881-123">-PSSession</span></span>
<span data-ttu-id="0c881-124">Wenn angegeben, wird der Befehl, der Computer in Azure einhauft, in den einzelnen PSSessions ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c881-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="0c881-125">HINWEIS: Dies funktioniert derzeit nur unter Windows.</span><span class="sxs-lookup"><span data-stu-id="0c881-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c881-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c881-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c881-127">Der Name der Ressourcengruppe, der Sie den Computer hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="0c881-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c881-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c881-128">-SubscriptionId</span></span>
<span data-ttu-id="0c881-129">Die ID des Abonnements, dem Sie den Computer hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="0c881-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c881-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c881-130">-Tag</span></span>
<span data-ttu-id="0c881-131">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="0c881-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c881-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c881-132">CommonParameters</span></span>
<span data-ttu-id="0c881-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c881-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c881-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c881-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c881-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c881-135">INPUTS</span></span>

## <span data-ttu-id="0c881-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c881-136">OUTPUTS</span></span>

## <span data-ttu-id="0c881-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0c881-137">NOTES</span></span>

<span data-ttu-id="0c881-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0c881-138">ALIASES</span></span>

## <span data-ttu-id="0c881-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0c881-139">RELATED LINKS</span></span>

