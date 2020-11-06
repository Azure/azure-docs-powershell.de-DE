---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 3da05194d74de1fe547beb66dea420a7f0e90155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481550"
---
# <span data-ttu-id="162b4-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="162b4-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="162b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="162b4-102">SYNOPSIS</span></span>
<span data-ttu-id="162b4-103">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="162b4-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="162b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="162b4-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="162b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="162b4-105">DESCRIPTION</span></span>
<span data-ttu-id="162b4-106">Verwenden Sie **Remove-AzureRmServiceFabricNodeType** , um alle Knoten aus einem bestimmten Knotentyp und dem Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="162b4-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="162b4-107">Dieser Befehl kann nicht zum Löschen des primären Knotentyps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="162b4-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="162b4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="162b4-108">EXAMPLES</span></span>

### <span data-ttu-id="162b4-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="162b4-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="162b4-110">Mit diesem Befehl wird NodeType "NT1" aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="162b4-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="162b4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="162b4-111">PARAMETERS</span></span>

### <span data-ttu-id="162b4-112">-Name</span><span class="sxs-lookup"><span data-stu-id="162b4-112">-Name</span></span>
<span data-ttu-id="162b4-113">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="162b4-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="162b4-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="162b4-114">-NodeType</span></span>
<span data-ttu-id="162b4-115">Der Name des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="162b4-115">The node type name.</span></span>

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

### <span data-ttu-id="162b4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="162b4-116">-ResourceGroupName</span></span>
<span data-ttu-id="162b4-117">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="162b4-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="162b4-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="162b4-118">-Confirm</span></span>
<span data-ttu-id="162b4-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="162b4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="162b4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="162b4-120">-WhatIf</span></span>
<span data-ttu-id="162b4-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="162b4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="162b4-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="162b4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="162b4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162b4-123">-DefaultProfile</span></span>
<span data-ttu-id="162b4-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="162b4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="162b4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162b4-125">CommonParameters</span></span>
<span data-ttu-id="162b4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="162b4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162b4-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="162b4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162b4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="162b4-128">INPUTS</span></span>

### <span data-ttu-id="162b4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="162b4-129">System.String</span></span>

## <span data-ttu-id="162b4-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="162b4-130">OUTPUTS</span></span>

### <span data-ttu-id="162b4-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="162b4-131">System.Object</span></span>

## <span data-ttu-id="162b4-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="162b4-132">NOTES</span></span>

## <span data-ttu-id="162b4-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="162b4-133">RELATED LINKS</span></span>

