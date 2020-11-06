---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 212e0c2ee4863c6d18873a717ff25f6940c34a15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481290"
---
# <span data-ttu-id="6f181-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="6f181-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="6f181-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f181-102">SYNOPSIS</span></span>
<span data-ttu-id="6f181-103">Entfernt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6f181-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f181-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f181-104">SYNTAX</span></span>

### <span data-ttu-id="6f181-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f181-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f181-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6f181-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f181-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f181-107">DESCRIPTION</span></span>
<span data-ttu-id="6f181-108">Das Cmdlet **Remove-AzureRmDataFactory** entfernt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6f181-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="6f181-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f181-109">EXAMPLES</span></span>

### <span data-ttu-id="6f181-110">Beispiel 1: Entfernen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="6f181-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="6f181-111">Mit diesem Befehl wird die Data Factory mit dem Namen WikiADF aus der Ressourcengruppe ADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f181-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="6f181-112">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="6f181-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="6f181-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f181-113">PARAMETERS</span></span>

### <span data-ttu-id="6f181-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f181-114">-DataFactory</span></span>
<span data-ttu-id="6f181-115">Gibt das zu entfernende **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6f181-115">Specifies the **PSDataFactory** object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f181-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f181-116">-DefaultProfile</span></span>
<span data-ttu-id="6f181-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6f181-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f181-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6f181-118">-Force</span></span>
<span data-ttu-id="6f181-119">Gibt an, dass dieses Cmdlet eine Data Factory entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="6f181-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="6f181-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6f181-120">-Name</span></span>
<span data-ttu-id="6f181-121">Gibt den Namen der Daten Factory an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f181-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f181-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f181-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f181-123">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6f181-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6f181-124">Mit diesem Cmdlet wird eine Data Factory aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6f181-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f181-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f181-125">-Confirm</span></span>
<span data-ttu-id="6f181-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f181-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f181-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f181-127">-WhatIf</span></span>
<span data-ttu-id="6f181-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f181-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f181-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f181-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f181-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f181-130">CommonParameters</span></span>
<span data-ttu-id="6f181-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f181-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f181-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f181-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f181-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f181-133">INPUTS</span></span>

### <span data-ttu-id="6f181-134">Keine</span><span class="sxs-lookup"><span data-stu-id="6f181-134">None</span></span>
<span data-ttu-id="6f181-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6f181-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f181-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f181-136">OUTPUTS</span></span>

### <span data-ttu-id="6f181-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f181-137">System.Boolean</span></span>

## <span data-ttu-id="6f181-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f181-138">NOTES</span></span>
* <span data-ttu-id="6f181-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="6f181-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6f181-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f181-140">RELATED LINKS</span></span>

[<span data-ttu-id="6f181-141">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="6f181-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="6f181-142">Neu – AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="6f181-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


