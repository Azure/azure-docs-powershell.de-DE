---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: 5b88342a91f015cd58da36f9b04d3a8a325ae239
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478218"
---
# <span data-ttu-id="2ccbb-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2ccbb-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="2ccbb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ccbb-102">SYNOPSIS</span></span>
<span data-ttu-id="2ccbb-103">Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ccbb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ccbb-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ccbb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ccbb-105">DESCRIPTION</span></span>
<span data-ttu-id="2ccbb-106">Verwenden Sie **Update-AzureRmServiceFabricReliability** , um die Zuverlässigkeit des primären Knotentyps in einem Cluster zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="2ccbb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ccbb-107">EXAMPLES</span></span>

### <span data-ttu-id="2ccbb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ccbb-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="2ccbb-109">Mit diesem Befehl wird die Zuverlässigkeitsstufe des primären Knotentyps in Silver geändert.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="2ccbb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ccbb-110">PARAMETERS</span></span>

### <span data-ttu-id="2ccbb-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="2ccbb-111">-AutoAddNode</span></span>
<span data-ttu-id="2ccbb-112">Automatisches Hinzufügen der Knotenanzahl beim Ändern der Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="2ccbb-112">Add node count automatically when changing reliability.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ccbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ccbb-113">-DefaultProfile</span></span>
<span data-ttu-id="2ccbb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ccbb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2ccbb-115">-Name</span></span>
<span data-ttu-id="2ccbb-116">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2ccbb-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="2ccbb-117">-ReliabilityLevel</span></span>
<span data-ttu-id="2ccbb-118">Zuverlässigkeitsstufe</span><span class="sxs-lookup"><span data-stu-id="2ccbb-118">Reliability tier.</span></span>

```yaml
Type: ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ccbb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ccbb-119">-ResourceGroupName</span></span>
<span data-ttu-id="2ccbb-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2ccbb-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ccbb-121">-Confirm</span></span>
<span data-ttu-id="2ccbb-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ccbb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ccbb-123">-WhatIf</span></span>
<span data-ttu-id="2ccbb-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ccbb-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ccbb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ccbb-126">CommonParameters</span></span>
<span data-ttu-id="2ccbb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ccbb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ccbb-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ccbb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ccbb-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ccbb-129">INPUTS</span></span>

### <span data-ttu-id="2ccbb-130">Microsoft. Azure. Commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="2ccbb-130">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="2ccbb-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2ccbb-131">System.Management.Automation.SwitchParameter</span></span>

<span data-ttu-id="2ccbb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ccbb-132">System.String</span></span>

## <span data-ttu-id="2ccbb-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ccbb-133">OUTPUTS</span></span>

### <span data-ttu-id="2ccbb-134">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="2ccbb-134">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="2ccbb-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ccbb-135">NOTES</span></span>

## <span data-ttu-id="2ccbb-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ccbb-136">RELATED LINKS</span></span>

