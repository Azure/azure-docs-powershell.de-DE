---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295792"
---
# <span data-ttu-id="aca00-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="aca00-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="aca00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aca00-102">SYNOPSIS</span></span>
<span data-ttu-id="aca00-103">Aktualisieren Sie die Netzwerk-ACL eines SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="aca00-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="aca00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aca00-104">SYNTAX</span></span>

### <span data-ttu-id="aca00-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aca00-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aca00-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aca00-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aca00-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aca00-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aca00-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aca00-108">DESCRIPTION</span></span>
<span data-ttu-id="aca00-109">Aktualisieren Sie die Netzwerk-ACL eines SignalR-Diensts, einschließlich der Standardaktion und der Netzwerk-Acls für öffentliche und private Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="aca00-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="aca00-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aca00-110">EXAMPLES</span></span>

### <span data-ttu-id="aca00-111">RESTAPI zulassen, ClientConnection für öffentliches Netzwerk und Standardaktion auf "Verweigern" festlegen</span><span class="sxs-lookup"><span data-stu-id="aca00-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
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

### <span data-ttu-id="aca00-112">Clientverbindung und Serververbindung für eine private Endpunktverbindung zulassen</span><span class="sxs-lookup"><span data-stu-id="aca00-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="aca00-113">Clientverbindung für öffentliches Netzwerk und private Endpunktverbindung verweigern</span><span class="sxs-lookup"><span data-stu-id="aca00-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="aca00-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aca00-114">PARAMETERS</span></span>

### <span data-ttu-id="aca00-115">-Allow</span><span class="sxs-lookup"><span data-stu-id="aca00-115">-Allow</span></span>
<span data-ttu-id="aca00-116">Zugelassene Netzwerk-ACLs</span><span class="sxs-lookup"><span data-stu-id="aca00-116">Allowed network ACLs</span></span>

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

### <span data-ttu-id="aca00-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aca00-117">-AsJob</span></span>
<span data-ttu-id="aca00-118">Führen Sie das Cmdlet im Hintergrundauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="aca00-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="aca00-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="aca00-119">-DefaultAction</span></span>
<span data-ttu-id="aca00-120">Standardaktion von SignalR-Netzwerk-ACLs, entweder zulassen oder verweigern.</span><span class="sxs-lookup"><span data-stu-id="aca00-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="aca00-121">Es entscheidet, ob Netzwerk-ACLs verweigert oder Netzwerk-ACLs wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="aca00-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="aca00-122">Wenn beispielsweise die Standardaktion zulässig ist, kommt es nur auf die Verweigern-ACLs an.</span><span class="sxs-lookup"><span data-stu-id="aca00-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

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

### <span data-ttu-id="aca00-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca00-123">-DefaultProfile</span></span>
<span data-ttu-id="aca00-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aca00-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aca00-125">-Verweigern</span><span class="sxs-lookup"><span data-stu-id="aca00-125">-Deny</span></span>
<span data-ttu-id="aca00-126">Netzwerk-ACLs verweigert</span><span class="sxs-lookup"><span data-stu-id="aca00-126">Denied network ACLs</span></span>

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

### <span data-ttu-id="aca00-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aca00-127">-InputObject</span></span>
<span data-ttu-id="aca00-128">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="aca00-128">The SignalR resource object.</span></span>

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

### <span data-ttu-id="aca00-129">-Name</span><span class="sxs-lookup"><span data-stu-id="aca00-129">-Name</span></span>
<span data-ttu-id="aca00-130">Der Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="aca00-130">The SignalR service name.</span></span>

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

### <span data-ttu-id="aca00-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="aca00-131">-PrivateEndpointName</span></span>
<span data-ttu-id="aca00-132">Namen der privaten Endpunkte, die aktualisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="aca00-132">Name(s) of private endpoint(s) to be updated</span></span>

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

### <span data-ttu-id="aca00-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="aca00-133">-PublicNetwork</span></span>
<span data-ttu-id="aca00-134">Aktualisieren von ACLs für öffentliche Netzwerke</span><span class="sxs-lookup"><span data-stu-id="aca00-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="aca00-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca00-135">-ResourceGroupName</span></span>
<span data-ttu-id="aca00-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aca00-136">The resource group name.</span></span>
<span data-ttu-id="aca00-137">Die Standardeinstellung wird verwendet, wenn sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aca00-137">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="aca00-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aca00-138">-ResourceId</span></span>
<span data-ttu-id="aca00-139">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="aca00-139">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="aca00-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aca00-140">-Confirm</span></span>
<span data-ttu-id="aca00-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aca00-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aca00-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aca00-142">-WhatIf</span></span>
<span data-ttu-id="aca00-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aca00-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aca00-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aca00-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aca00-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca00-145">CommonParameters</span></span>
<span data-ttu-id="aca00-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aca00-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca00-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aca00-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca00-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aca00-148">INPUTS</span></span>

### <span data-ttu-id="aca00-149">System.String</span><span class="sxs-lookup"><span data-stu-id="aca00-149">System.String</span></span>

## <span data-ttu-id="aca00-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aca00-150">OUTPUTS</span></span>

### <span data-ttu-id="aca00-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="aca00-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="aca00-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aca00-152">NOTES</span></span>

## <span data-ttu-id="aca00-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aca00-153">RELATED LINKS</span></span>
