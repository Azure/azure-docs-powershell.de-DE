---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: 0d29c556af0706297db630c05d9d1d86a384db8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824716"
---
# <span data-ttu-id="ae669-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ae669-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="ae669-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae669-102">SYNOPSIS</span></span>
<span data-ttu-id="ae669-103">Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="ae669-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="ae669-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae669-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae669-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae669-105">DESCRIPTION</span></span>
<span data-ttu-id="ae669-106">Hinzufügen eines neuen Knotentyps zu einem vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="ae669-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="ae669-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae669-107">EXAMPLES</span></span>

### <span data-ttu-id="ae669-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae669-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="ae669-109">Mit diesem Befehl wird ein neuer NodeType "N2" mit der Kapazität 5 hinzugefügt, und der VM-Administratorname lautet "Adminname".</span><span class="sxs-lookup"><span data-stu-id="ae669-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="ae669-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae669-110">PARAMETERS</span></span>

### <span data-ttu-id="ae669-111">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="ae669-111">-Capacity</span></span>
<span data-ttu-id="ae669-112">Kapazität</span><span class="sxs-lookup"><span data-stu-id="ae669-112">Capacity</span></span>

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

### <span data-ttu-id="ae669-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae669-113">-DefaultProfile</span></span>
<span data-ttu-id="ae669-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae669-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae669-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ae669-115">-DurabilityLevel</span></span>
<span data-ttu-id="ae669-116">Geben Sie die Dauer Haltbarkeits Stufe des NodeType an.</span><span class="sxs-lookup"><span data-stu-id="ae669-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="ae669-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ae669-117">-Name</span></span>
<span data-ttu-id="ae669-118">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="ae669-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="ae669-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ae669-119">-NodeType</span></span>
<span data-ttu-id="ae669-120">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="ae669-120">The node type name</span></span>

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

### <span data-ttu-id="ae669-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae669-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae669-122">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ae669-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ae669-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="ae669-123">-Tier</span></span>
<span data-ttu-id="ae669-124">VM-SKU-Ebene</span><span class="sxs-lookup"><span data-stu-id="ae669-124">Vm Sku Tier</span></span>

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

### <span data-ttu-id="ae669-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="ae669-125">-VmPassword</span></span>
<span data-ttu-id="ae669-126">Das Kennwort für die Anmeldung beim virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="ae669-126">The password for login to the Vm</span></span>

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

### <span data-ttu-id="ae669-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="ae669-127">-VmSku</span></span>
<span data-ttu-id="ae669-128">Der SKU-Name</span><span class="sxs-lookup"><span data-stu-id="ae669-128">The sku name</span></span>

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

### <span data-ttu-id="ae669-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="ae669-129">-VmUserName</span></span>
<span data-ttu-id="ae669-130">Der Benutzername für die Protokollierung bei VM</span><span class="sxs-lookup"><span data-stu-id="ae669-130">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="ae669-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae669-131">-Confirm</span></span>
<span data-ttu-id="ae669-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae669-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae669-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae669-133">-WhatIf</span></span>
<span data-ttu-id="ae669-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae669-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae669-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae669-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae669-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae669-136">CommonParameters</span></span>
<span data-ttu-id="ae669-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae669-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae669-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae669-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae669-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae669-139">INPUTS</span></span>

### <span data-ttu-id="ae669-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ae669-140">System.String</span></span>

### <span data-ttu-id="ae669-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ae669-141">System.Int32</span></span>

### <span data-ttu-id="ae669-142">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ae669-142">System.Security.SecureString</span></span>

### <span data-ttu-id="ae669-143">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ae669-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="ae669-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae669-144">OUTPUTS</span></span>

### <span data-ttu-id="ae669-145">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ae669-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ae669-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae669-146">NOTES</span></span>

## <span data-ttu-id="ae669-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae669-147">RELATED LINKS</span></span>
