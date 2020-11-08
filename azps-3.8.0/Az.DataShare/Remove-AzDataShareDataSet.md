---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 1d9566bedbb3e7479f1e9e00c3cc179a225cab2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003074"
---
# <span data-ttu-id="0d4d6-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="0d4d6-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="0d4d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4d6-103">Entfernt eine Daten satzzuordnung</span><span class="sxs-lookup"><span data-stu-id="0d4d6-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="0d4d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d4d6-104">SYNTAX</span></span>

### <span data-ttu-id="0d4d6-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d4d6-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4d6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4d6-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4d6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4d6-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d4d6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d4d6-108">DESCRIPTION</span></span>
<span data-ttu-id="0d4d6-109">Das Cmdlet **Remove-AzDataShareDataSet** entfernt ein DataSet.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="0d4d6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d4d6-110">EXAMPLES</span></span>

### <span data-ttu-id="0d4d6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d4d6-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="0d4d6-112">Mit diesen Befehlen wird das DataSet DS aus Freigabe-WikiAds entfernt.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="0d4d6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d4d6-113">PARAMETERS</span></span>

### <span data-ttu-id="0d4d6-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="0d4d6-114">-AccountName</span></span>
<span data-ttu-id="0d4d6-115">Name des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="0d4d6-115">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d4d6-116">-DefaultProfile</span></span>
<span data-ttu-id="0d4d6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d4d6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d4d6-118">-InputObject</span></span>
<span data-ttu-id="0d4d6-119">Das Azure-Datensatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4d6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0d4d6-120">-Name</span></span>
<span data-ttu-id="0d4d6-121">Name des Azure-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4d6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d4d6-122">-PassThru</span></span>
<span data-ttu-id="0d4d6-123">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="0d4d6-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="0d4d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d4d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d4d6-125">Der Name der Ressourcengruppe des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-125">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4d6-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0d4d6-126">-ResourceId</span></span>
<span data-ttu-id="0d4d6-127">Die Ressourcen-ID der Azure-Datengruppe.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-127">The resource id of the azure data set.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4d6-128">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="0d4d6-128">-ShareName</span></span>
<span data-ttu-id="0d4d6-129">Name der Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-129">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4d6-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d4d6-130">-Confirm</span></span>
<span data-ttu-id="0d4d6-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d4d6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d4d6-132">-WhatIf</span></span>
<span data-ttu-id="0d4d6-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d4d6-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d4d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4d6-135">CommonParameters</span></span>
<span data-ttu-id="0d4d6-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4d6-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d4d6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4d6-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d4d6-138">INPUTS</span></span>

### <span data-ttu-id="0d4d6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0d4d6-139">System.String</span></span>

### <span data-ttu-id="0d4d6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="0d4d6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="0d4d6-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d4d6-141">OUTPUTS</span></span>

### <span data-ttu-id="0d4d6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d4d6-142">System.Boolean</span></span>

## <span data-ttu-id="0d4d6-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d4d6-143">NOTES</span></span>

## <span data-ttu-id="0d4d6-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d4d6-144">RELATED LINKS</span></span>
