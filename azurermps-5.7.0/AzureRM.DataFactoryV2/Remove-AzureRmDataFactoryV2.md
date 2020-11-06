---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 330bcf3622faa515a58ea8f1e087d1383b9f154a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476834"
---
# <span data-ttu-id="b1b1a-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b1b1a-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="b1b1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b1a-103">Entfernt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1b1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1b1a-104">SYNTAX</span></span>

### <span data-ttu-id="b1b1a-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1b1a-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b1a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b1b1a-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b1a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1b1a-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1b1a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1b1a-108">DESCRIPTION</span></span>
<span data-ttu-id="b1b1a-109">Das Remove-AzureRmDataFactoryV2-Cmdlet entfernt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="b1b1a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1b1a-110">EXAMPLES</span></span>

### <span data-ttu-id="b1b1a-111">Beispiel 1: Entfernen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="b1b1a-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="b1b1a-112">Mit diesem Befehl wird die Data Factory mit dem Namen WikiADF aus der Ressourcengruppe ADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="b1b1a-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="b1b1a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1b1a-114">PARAMETERS</span></span>

### <span data-ttu-id="b1b1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b1a-115">-DefaultProfile</span></span>
<span data-ttu-id="b1b1a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1b1a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b1b1a-117">-Force</span></span>
<span data-ttu-id="b1b1a-118">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-118">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b1a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1b1a-119">-InputObject</span></span>
<span data-ttu-id="b1b1a-120">Gibt das zu entfernende DataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1b1a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b1b1a-121">-Name</span></span>
<span data-ttu-id="b1b1a-122">Gibt den Namen der Daten Factory an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b1a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b1a-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1b1a-124">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b1b1a-125">Mit diesem Cmdlet wird eine Data Factory aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b1a-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b1b1a-126">-ResourceId</span></span>
<span data-ttu-id="b1b1a-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1b1a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1b1a-128">-Confirm</span></span>
<span data-ttu-id="b1b1a-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b1a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b1a-130">-WhatIf</span></span>
<span data-ttu-id="b1b1a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b1b1a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b1a-132">CommonParameters</span></span>
<span data-ttu-id="b1b1a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b1a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b1a-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b1a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b1a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1b1a-135">INPUTS</span></span>

### <span data-ttu-id="b1b1a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b1b1a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="b1b1a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b1b1a-137">System.String</span></span>

## <span data-ttu-id="b1b1a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1b1a-138">OUTPUTS</span></span>

### <span data-ttu-id="b1b1a-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="b1b1a-139">System.Object</span></span>

## <span data-ttu-id="b1b1a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1b1a-140">NOTES</span></span>
<span data-ttu-id="b1b1a-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="b1b1a-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b1b1a-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1b1a-142">RELATED LINKS</span></span>

[<span data-ttu-id="b1b1a-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b1b1a-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="b1b1a-144">Satz-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b1b1a-144">Set-AzureRmDataFactoryV2</span></span>]()
