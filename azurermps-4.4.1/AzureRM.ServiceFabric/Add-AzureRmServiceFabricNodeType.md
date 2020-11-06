---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 305e406a3f2ef723eb0431b495106bb688ffe61c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500694"
---
# <span data-ttu-id="e574a-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e574a-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="e574a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e574a-102">SYNOPSIS</span></span>
<span data-ttu-id="e574a-103">Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="e574a-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e574a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e574a-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -Capacity <Int32> -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e574a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e574a-105">DESCRIPTION</span></span>
<span data-ttu-id="e574a-106">Hinzufügen eines neuen Knotentyps zu einem vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="e574a-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="e574a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e574a-107">EXAMPLES</span></span>

### <span data-ttu-id="e574a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e574a-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="e574a-109">Mit diesem Befehl wird ein neuer NodeType "N2" mit der Kapazität 5 hinzugefügt, und der VM-Administratorname lautet "Adminname".</span><span class="sxs-lookup"><span data-stu-id="e574a-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="e574a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e574a-110">PARAMETERS</span></span>

### <span data-ttu-id="e574a-111">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="e574a-111">-Capacity</span></span>
<span data-ttu-id="e574a-112">Kapazität</span><span class="sxs-lookup"><span data-stu-id="e574a-112">Capacity</span></span>

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

### <span data-ttu-id="e574a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e574a-113">-Name</span></span>
<span data-ttu-id="e574a-114">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e574a-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e574a-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="e574a-115">-NodeType</span></span>
<span data-ttu-id="e574a-116">Der Name des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="e574a-116">The node type name.</span></span>

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

### <span data-ttu-id="e574a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e574a-117">-ResourceGroupName</span></span>
<span data-ttu-id="e574a-118">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e574a-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e574a-119">-Tier</span><span class="sxs-lookup"><span data-stu-id="e574a-119">-Tier</span></span>
<span data-ttu-id="e574a-120">VM-SKU-Ebene</span><span class="sxs-lookup"><span data-stu-id="e574a-120">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="e574a-121">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="e574a-121">-DurabilityLevel</span></span>
<span data-ttu-id="e574a-122">Geben Sie die Dauer Haltbarkeits Stufe des NodeType an.</span><span class="sxs-lookup"><span data-stu-id="e574a-122">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="e574a-123">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="e574a-123">-VmPassword</span></span>
<span data-ttu-id="e574a-124">Das Kennwort für die Anmeldung bei der VM.</span><span class="sxs-lookup"><span data-stu-id="e574a-124">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="e574a-125">-VmSku</span><span class="sxs-lookup"><span data-stu-id="e574a-125">-VmSku</span></span>
<span data-ttu-id="e574a-126">Der SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="e574a-126">The sku name.</span></span>

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

### <span data-ttu-id="e574a-127">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="e574a-127">-VmUserName</span></span>
<span data-ttu-id="e574a-128">Der Benutzername für die Anmeldung bei VM.</span><span class="sxs-lookup"><span data-stu-id="e574a-128">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="e574a-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e574a-129">-Confirm</span></span>
<span data-ttu-id="e574a-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e574a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e574a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e574a-131">-WhatIf</span></span>
<span data-ttu-id="e574a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e574a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e574a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e574a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e574a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e574a-134">-DefaultProfile</span></span>
<span data-ttu-id="e574a-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e574a-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e574a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e574a-136">CommonParameters</span></span>
<span data-ttu-id="e574a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e574a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e574a-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e574a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e574a-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e574a-139">INPUTS</span></span>

### <span data-ttu-id="e574a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e574a-140">System.String</span></span>
<span data-ttu-id="e574a-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e574a-141">System.Int32</span></span>

## <span data-ttu-id="e574a-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e574a-142">OUTPUTS</span></span>

### <span data-ttu-id="e574a-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="e574a-143">System.Object</span></span>

## <span data-ttu-id="e574a-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e574a-144">NOTES</span></span>

## <span data-ttu-id="e574a-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e574a-145">RELATED LINKS</span></span>

