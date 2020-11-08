---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995175"
---
# <span data-ttu-id="240cc-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="240cc-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="240cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="240cc-102">SYNOPSIS</span></span>
<span data-ttu-id="240cc-103">Entfernt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="240cc-103">Removes a data factory.</span></span>

## <span data-ttu-id="240cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="240cc-104">SYNTAX</span></span>

### <span data-ttu-id="240cc-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="240cc-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240cc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="240cc-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240cc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="240cc-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="240cc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="240cc-108">DESCRIPTION</span></span>
<span data-ttu-id="240cc-109">Das Remove-AzDataFactoryV2-Cmdlet entfernt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="240cc-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="240cc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="240cc-110">EXAMPLES</span></span>

### <span data-ttu-id="240cc-111">Beispiel 1: Entfernen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="240cc-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="240cc-112">Mit diesem Befehl wird die Data Factory mit dem Namen WikiADF aus der Ressourcengruppe ADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="240cc-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="240cc-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="240cc-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="240cc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="240cc-114">PARAMETERS</span></span>

### <span data-ttu-id="240cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240cc-115">-DefaultProfile</span></span>
<span data-ttu-id="240cc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="240cc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="240cc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="240cc-117">-Force</span></span>
<span data-ttu-id="240cc-118">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="240cc-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="240cc-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="240cc-119">-InputObject</span></span>
<span data-ttu-id="240cc-120">Gibt das zu entfernende DataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="240cc-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="240cc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="240cc-121">-Name</span></span>
<span data-ttu-id="240cc-122">Gibt den Namen der Daten Factory an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="240cc-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="240cc-124">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="240cc-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="240cc-125">Mit diesem Cmdlet wird eine Data Factory aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="240cc-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240cc-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="240cc-126">-ResourceId</span></span>
<span data-ttu-id="240cc-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="240cc-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240cc-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="240cc-128">-Confirm</span></span>
<span data-ttu-id="240cc-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="240cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="240cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="240cc-130">-WhatIf</span></span>
<span data-ttu-id="240cc-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="240cc-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="240cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240cc-132">CommonParameters</span></span>
<span data-ttu-id="240cc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="240cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240cc-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="240cc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240cc-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="240cc-135">INPUTS</span></span>

### <span data-ttu-id="240cc-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="240cc-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="240cc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="240cc-137">System.String</span></span>

## <span data-ttu-id="240cc-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="240cc-138">OUTPUTS</span></span>

### <span data-ttu-id="240cc-139">System. void</span><span class="sxs-lookup"><span data-stu-id="240cc-139">System.Void</span></span>

## <span data-ttu-id="240cc-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="240cc-140">NOTES</span></span>
<span data-ttu-id="240cc-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="240cc-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="240cc-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="240cc-142">RELATED LINKS</span></span>

[<span data-ttu-id="240cc-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="240cc-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="240cc-144">Satz-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="240cc-144">Set-AzDataFactoryV2</span></span>]()
