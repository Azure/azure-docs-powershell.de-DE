---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: 24552172c0f793c8414b5abfc9e6a66c747915d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920283"
---
# <span data-ttu-id="161bd-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="161bd-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="161bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="161bd-102">SYNOPSIS</span></span>
<span data-ttu-id="161bd-103">Aktualisieren Sie die Netzwerk-ACL eines SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="161bd-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="161bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="161bd-104">SYNTAX</span></span>

### <span data-ttu-id="161bd-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="161bd-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="161bd-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="161bd-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="161bd-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="161bd-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="161bd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="161bd-108">DESCRIPTION</span></span>
<span data-ttu-id="161bd-109">Aktualisieren Sie die Netzwerk-ACL eines SignalR-Diensts, einschließlich der Standardaktion und der Netzwerk-Acls für öffentliche und private Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="161bd-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="161bd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="161bd-110">EXAMPLES</span></span>

### <span data-ttu-id="161bd-111">RESTAPI zulassen,ClientVerbinden für öffentliches Netzwerk zulassen und Standardaktion auf Verweigern festlegen</span><span class="sxs-lookup"><span data-stu-id="161bd-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="161bd-112">Zulassen der Client- und Serververbindung für eine private Endpunktverbindung</span><span class="sxs-lookup"><span data-stu-id="161bd-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="161bd-113">Clientverbindung für öffentliches Netzwerk und private Endpunktverbindung verweigern</span><span class="sxs-lookup"><span data-stu-id="161bd-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="161bd-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="161bd-114">PARAMETERS</span></span>

### <span data-ttu-id="161bd-115">-Zulassen</span><span class="sxs-lookup"><span data-stu-id="161bd-115">-Allow</span></span>
<span data-ttu-id="161bd-116">Zulässige Netzwerk-ACLs</span><span class="sxs-lookup"><span data-stu-id="161bd-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="161bd-117">-AsJob</span></span>
<span data-ttu-id="161bd-118">Führen Sie das Cmdlet im Hintergrundauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="161bd-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="161bd-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="161bd-119">-DefaultAction</span></span>
<span data-ttu-id="161bd-120">Standardaktion von SignalR-Netzwerk-ACLs, entweder zulassen oder verweigern.</span><span class="sxs-lookup"><span data-stu-id="161bd-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="161bd-121">Sie entscheidet, ob Netzwerk-ACLs verweigert oder Netzwerk-ACLs zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="161bd-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="161bd-122">Wenn beispielsweise die Standardaktion zulässig ist, ist nur die Verweigern-ACLs wichtig.</span><span class="sxs-lookup"><span data-stu-id="161bd-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161bd-123">-DefaultProfile</span></span>
<span data-ttu-id="161bd-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="161bd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="161bd-125">-Verweigern</span><span class="sxs-lookup"><span data-stu-id="161bd-125">-Deny</span></span>
<span data-ttu-id="161bd-126">Verweigerte Netzwerk-ACLs</span><span class="sxs-lookup"><span data-stu-id="161bd-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="161bd-127">-InputObject</span></span>
<span data-ttu-id="161bd-128">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="161bd-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-129">-Name</span><span class="sxs-lookup"><span data-stu-id="161bd-129">-Name</span></span>
<span data-ttu-id="161bd-130">Der Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="161bd-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="161bd-131">-PrivateEndpointName</span></span>
<span data-ttu-id="161bd-132">Name(n) privater Endpunkte, die aktualisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="161bd-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="161bd-133">-PublicNetwork</span></span>
<span data-ttu-id="161bd-134">Aktualisieren von ACLs für öffentliche Netzwerke</span><span class="sxs-lookup"><span data-stu-id="161bd-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="161bd-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161bd-135">-ResourceGroupName</span></span>
<span data-ttu-id="161bd-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="161bd-136">The resource group name.</span></span>
<span data-ttu-id="161bd-137">Die Standardeinstellung wird verwendet, wenn sie nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="161bd-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="161bd-138">-ResourceId</span></span>
<span data-ttu-id="161bd-139">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="161bd-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="161bd-140">-Confirm</span></span>
<span data-ttu-id="161bd-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="161bd-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="161bd-142">-WhatIf</span></span>
<span data-ttu-id="161bd-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="161bd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="161bd-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="161bd-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161bd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161bd-145">CommonParameters</span></span>
<span data-ttu-id="161bd-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="161bd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161bd-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="161bd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161bd-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="161bd-148">INPUTS</span></span>

### <span data-ttu-id="161bd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="161bd-149">System.String</span></span>

## <span data-ttu-id="161bd-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="161bd-150">OUTPUTS</span></span>

### <span data-ttu-id="161bd-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="161bd-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="161bd-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="161bd-152">NOTES</span></span>

## <span data-ttu-id="161bd-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="161bd-153">RELATED LINKS</span></span>
