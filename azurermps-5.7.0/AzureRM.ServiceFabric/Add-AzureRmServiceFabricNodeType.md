---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 0bae150e60332e4f1bb0ee4f2ee67699c13eb5e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478245"
---
# <span data-ttu-id="bcac1-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="bcac1-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="bcac1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bcac1-102">SYNOPSIS</span></span>
<span data-ttu-id="bcac1-103">Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="bcac1-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcac1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcac1-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcac1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bcac1-105">DESCRIPTION</span></span>
<span data-ttu-id="bcac1-106">Hinzufügen eines neuen Knotentyps zu einem vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="bcac1-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="bcac1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bcac1-107">EXAMPLES</span></span>

### <span data-ttu-id="bcac1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bcac1-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="bcac1-109">Mit diesem Befehl wird ein neuer NodeType "N2" mit der Kapazität 5 hinzugefügt, und der VM-Administratorname lautet "Adminname".</span><span class="sxs-lookup"><span data-stu-id="bcac1-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="bcac1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcac1-110">PARAMETERS</span></span>

### <span data-ttu-id="bcac1-111">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="bcac1-111">-Capacity</span></span>
<span data-ttu-id="bcac1-112">Kapazität</span><span class="sxs-lookup"><span data-stu-id="bcac1-112">Capacity</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcac1-113">-DefaultProfile</span></span>
<span data-ttu-id="bcac1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bcac1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="bcac1-115">-DurabilityLevel</span></span>
<span data-ttu-id="bcac1-116">Geben Sie die Dauer Haltbarkeits Stufe des NodeType an.</span><span class="sxs-lookup"><span data-stu-id="bcac1-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: 
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bcac1-117">-Name</span></span>
<span data-ttu-id="bcac1-118">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="bcac1-118">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="bcac1-119">-NodeType</span></span>
<span data-ttu-id="bcac1-120">Der Name des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="bcac1-120">The node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcac1-121">-ResourceGroupName</span></span>
<span data-ttu-id="bcac1-122">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="bcac1-122">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="bcac1-123">-Tier</span></span>
<span data-ttu-id="bcac1-124">VM-SKU-Ebene</span><span class="sxs-lookup"><span data-stu-id="bcac1-124">Vm Sku Tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="bcac1-125">-VmPassword</span></span>
<span data-ttu-id="bcac1-126">Das Kennwort für die Anmeldung bei der VM.</span><span class="sxs-lookup"><span data-stu-id="bcac1-126">The password of login to the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="bcac1-127">-VmSku</span></span>
<span data-ttu-id="bcac1-128">Der SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="bcac1-128">The sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="bcac1-129">-VmUserName</span></span>
<span data-ttu-id="bcac1-130">Der Benutzername für die Anmeldung bei VM.</span><span class="sxs-lookup"><span data-stu-id="bcac1-130">The user name for login to Vm.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bcac1-131">-Confirm</span></span>
<span data-ttu-id="bcac1-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcac1-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcac1-133">-WhatIf</span></span>
<span data-ttu-id="bcac1-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcac1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcac1-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcac1-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcac1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcac1-136">CommonParameters</span></span>
<span data-ttu-id="bcac1-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcac1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcac1-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcac1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcac1-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bcac1-139">INPUTS</span></span>

### <span data-ttu-id="bcac1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bcac1-140">System.String</span></span>
<span data-ttu-id="bcac1-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bcac1-141">System.Int32</span></span>

## <span data-ttu-id="bcac1-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bcac1-142">OUTPUTS</span></span>

### <span data-ttu-id="bcac1-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="bcac1-143">System.Object</span></span>

## <span data-ttu-id="bcac1-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="bcac1-144">NOTES</span></span>

## <span data-ttu-id="bcac1-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bcac1-145">RELATED LINKS</span></span>

