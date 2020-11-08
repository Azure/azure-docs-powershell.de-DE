---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008544"
---
# <span data-ttu-id="cc9ea-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="cc9ea-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="cc9ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9ea-103">Entfernt eine Daten satzzuordnung</span><span class="sxs-lookup"><span data-stu-id="cc9ea-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="cc9ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc9ea-104">SYNTAX</span></span>

### <span data-ttu-id="cc9ea-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc9ea-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc9ea-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc9ea-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc9ea-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc9ea-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc9ea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc9ea-108">DESCRIPTION</span></span>
<span data-ttu-id="cc9ea-109">Das Cmdlet **Remove-AzDataShareDataSet** entfernt ein DataSet.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="cc9ea-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc9ea-110">EXAMPLES</span></span>

### <span data-ttu-id="cc9ea-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc9ea-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="cc9ea-112">Mit diesen Befehlen wird das DataSet DS aus Freigabe-WikiAds entfernt.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="cc9ea-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc9ea-113">PARAMETERS</span></span>

### <span data-ttu-id="cc9ea-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="cc9ea-114">-AccountName</span></span>
<span data-ttu-id="cc9ea-115">Name des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="cc9ea-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="cc9ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9ea-116">-DefaultProfile</span></span>
<span data-ttu-id="cc9ea-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc9ea-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc9ea-118">-InputObject</span></span>
<span data-ttu-id="cc9ea-119">Das Azure-Datensatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-119">The azure data set object.</span></span>


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

### <span data-ttu-id="cc9ea-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cc9ea-120">-Name</span></span>
<span data-ttu-id="cc9ea-121">Name des Azure-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-121">Azure data set name.</span></span>

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

### <span data-ttu-id="cc9ea-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc9ea-122">-PassThru</span></span>
<span data-ttu-id="cc9ea-123">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="cc9ea-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="cc9ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc9ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="cc9ea-125">Der Name der Ressourcengruppe des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="cc9ea-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cc9ea-126">-ResourceId</span></span>
<span data-ttu-id="cc9ea-127">Die Ressourcen-ID der Azure-Datengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="cc9ea-128">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="cc9ea-128">-ShareName</span></span>
<span data-ttu-id="cc9ea-129">Name der Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-129">Azure data share name.</span></span>

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

### <span data-ttu-id="cc9ea-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc9ea-130">-Confirm</span></span>
<span data-ttu-id="cc9ea-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc9ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc9ea-132">-WhatIf</span></span>
<span data-ttu-id="cc9ea-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc9ea-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc9ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9ea-135">CommonParameters</span></span>
<span data-ttu-id="cc9ea-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc9ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9ea-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc9ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9ea-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc9ea-138">INPUTS</span></span>

### <span data-ttu-id="cc9ea-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cc9ea-139">System.String</span></span>

### <span data-ttu-id="cc9ea-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="cc9ea-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="cc9ea-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc9ea-141">OUTPUTS</span></span>

### <span data-ttu-id="cc9ea-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc9ea-142">System.Boolean</span></span>

## <span data-ttu-id="cc9ea-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc9ea-143">NOTES</span></span>

## <span data-ttu-id="cc9ea-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc9ea-144">RELATED LINKS</span></span>
