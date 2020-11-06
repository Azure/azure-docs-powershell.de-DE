---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 573dd2f4681ae140fbe98de5d9a7e9df4e2dc764
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482018"
---
# <span data-ttu-id="ef75a-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ef75a-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="ef75a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef75a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef75a-103">Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="ef75a-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef75a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef75a-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef75a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef75a-105">DESCRIPTION</span></span>
<span data-ttu-id="ef75a-106">Hinzufügen eines neuen Knotentyps zu einem vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="ef75a-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="ef75a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef75a-107">EXAMPLES</span></span>

### <span data-ttu-id="ef75a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef75a-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="ef75a-109">Mit diesem Befehl wird ein neuer NodeType "N2" mit der Kapazität 5 hinzugefügt, und der VM-Administratorname lautet "Adminname".</span><span class="sxs-lookup"><span data-stu-id="ef75a-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="ef75a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef75a-110">PARAMETERS</span></span>

### <span data-ttu-id="ef75a-111">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="ef75a-111">-Capacity</span></span>
<span data-ttu-id="ef75a-112">Kapazität</span><span class="sxs-lookup"><span data-stu-id="ef75a-112">Capacity</span></span>

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

### <span data-ttu-id="ef75a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef75a-113">-DefaultProfile</span></span>
<span data-ttu-id="ef75a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef75a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef75a-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ef75a-115">-DurabilityLevel</span></span>
<span data-ttu-id="ef75a-116">Geben Sie die Dauer Haltbarkeits Stufe des NodeType an.</span><span class="sxs-lookup"><span data-stu-id="ef75a-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="ef75a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ef75a-117">-Name</span></span>
<span data-ttu-id="ef75a-118">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ef75a-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ef75a-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ef75a-119">-NodeType</span></span>
<span data-ttu-id="ef75a-120">Der Name des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="ef75a-120">The node type name.</span></span>

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

### <span data-ttu-id="ef75a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef75a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef75a-122">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ef75a-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ef75a-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="ef75a-123">-Tier</span></span>
<span data-ttu-id="ef75a-124">VM-SKU-Ebene</span><span class="sxs-lookup"><span data-stu-id="ef75a-124">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="ef75a-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="ef75a-125">-VmPassword</span></span>
<span data-ttu-id="ef75a-126">Das Kennwort für die Anmeldung bei der VM.</span><span class="sxs-lookup"><span data-stu-id="ef75a-126">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="ef75a-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="ef75a-127">-VmSku</span></span>
<span data-ttu-id="ef75a-128">Der SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="ef75a-128">The sku name.</span></span>

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

### <span data-ttu-id="ef75a-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="ef75a-129">-VmUserName</span></span>
<span data-ttu-id="ef75a-130">Der Benutzername für die Anmeldung bei VM.</span><span class="sxs-lookup"><span data-stu-id="ef75a-130">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="ef75a-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef75a-131">-Confirm</span></span>
<span data-ttu-id="ef75a-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef75a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef75a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef75a-133">-WhatIf</span></span>
<span data-ttu-id="ef75a-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef75a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef75a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef75a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef75a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef75a-136">CommonParameters</span></span>
<span data-ttu-id="ef75a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef75a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef75a-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef75a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef75a-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef75a-139">INPUTS</span></span>

### <span data-ttu-id="ef75a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ef75a-140">System.String</span></span>
<span data-ttu-id="ef75a-141">Parameter: NodeType (ByValue), Tier (ByValue), VmSku (ByValue), VmUserName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef75a-141">Parameters: NodeType (ByValue), Tier (ByValue), VmSku (ByValue), VmUserName (ByValue)</span></span>

### <span data-ttu-id="ef75a-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ef75a-142">System.Int32</span></span>
<span data-ttu-id="ef75a-143">Parameter: Capacity (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef75a-143">Parameters: Capacity (ByValue)</span></span>

### <span data-ttu-id="ef75a-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ef75a-144">System.Security.SecureString</span></span>
<span data-ttu-id="ef75a-145">Parameter: VmPassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef75a-145">Parameters: VmPassword (ByValue)</span></span>

### <span data-ttu-id="ef75a-146">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ef75a-146">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="ef75a-147">Parameter: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef75a-147">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="ef75a-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef75a-148">OUTPUTS</span></span>

### <span data-ttu-id="ef75a-149">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ef75a-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ef75a-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef75a-150">NOTES</span></span>

## <span data-ttu-id="ef75a-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef75a-151">RELATED LINKS</span></span>
