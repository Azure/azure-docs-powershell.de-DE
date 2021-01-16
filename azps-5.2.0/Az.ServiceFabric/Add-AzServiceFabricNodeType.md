---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: de512f636b0a326029981e199b13926a9fc5824a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303536"
---
# <span data-ttu-id="f7d23-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f7d23-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="f7d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d23-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d23-103">Fügen Sie dem vorhandenen Cluster einen neuen Knotentyp hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7d23-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="f7d23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7d23-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d23-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7d23-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d23-106">Fügen Sie einem vorhandenen Cluster einen neuen Knotentyp hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7d23-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="f7d23-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7d23-107">EXAMPLES</span></span>

### <span data-ttu-id="f7d23-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7d23-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="f7d23-109">Mit diesem Befehl wird ein neuer NodeType 'n2' mit einer Kapazität von 5 hinzugefügt, und der Name des virtuellen Admins ist "adminName".</span><span class="sxs-lookup"><span data-stu-id="f7d23-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="f7d23-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7d23-110">PARAMETERS</span></span>

### <span data-ttu-id="f7d23-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="f7d23-111">-Capacity</span></span>
<span data-ttu-id="f7d23-112">Kapazität</span><span class="sxs-lookup"><span data-stu-id="f7d23-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d23-113">-DefaultProfile</span></span>
<span data-ttu-id="f7d23-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7d23-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d23-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="f7d23-115">-DurabilityLevel</span></span>
<span data-ttu-id="f7d23-116">Geben Sie die Dauer des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="f7d23-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases:
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d23-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f7d23-117">-Name</span></span>
<span data-ttu-id="f7d23-118">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="f7d23-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d23-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="f7d23-119">-NodeType</span></span>
<span data-ttu-id="f7d23-120">Der Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="f7d23-120">The node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d23-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d23-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7d23-122">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f7d23-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d23-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="f7d23-123">-Tier</span></span>
<span data-ttu-id="f7d23-124">Vm Sku Tier</span><span class="sxs-lookup"><span data-stu-id="f7d23-124">Vm Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d23-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="f7d23-125">-VmPassword</span></span>
<span data-ttu-id="f7d23-126">Das Kennwort für die Anmeldung bei der Vm</span><span class="sxs-lookup"><span data-stu-id="f7d23-126">The password for login to the Vm</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d23-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="f7d23-127">-VmSku</span></span>
<span data-ttu-id="f7d23-128">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="f7d23-128">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d23-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="f7d23-129">-VmUserName</span></span>
<span data-ttu-id="f7d23-130">Der Benutzername für die Protokollierung bei Vm</span><span class="sxs-lookup"><span data-stu-id="f7d23-130">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d23-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7d23-131">-Confirm</span></span>
<span data-ttu-id="f7d23-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7d23-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d23-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f7d23-133">-WhatIf</span></span>
<span data-ttu-id="f7d23-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7d23-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d23-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7d23-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d23-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d23-136">CommonParameters</span></span>
<span data-ttu-id="f7d23-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d23-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d23-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7d23-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d23-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7d23-139">INPUTS</span></span>

### <span data-ttu-id="f7d23-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f7d23-140">System.String</span></span>

### <span data-ttu-id="f7d23-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f7d23-141">System.Int32</span></span>

### <span data-ttu-id="f7d23-142">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="f7d23-142">System.Security.SecureString</span></span>

### <span data-ttu-id="f7d23-143">Microsoft.Azure.Commands.ServiceFabric.Models.222</span><span class="sxs-lookup"><span data-stu-id="f7d23-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="f7d23-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7d23-144">OUTPUTS</span></span>

### <span data-ttu-id="f7d23-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="f7d23-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f7d23-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7d23-146">NOTES</span></span>

## <span data-ttu-id="f7d23-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7d23-147">RELATED LINKS</span></span>
