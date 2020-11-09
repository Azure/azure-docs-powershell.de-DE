---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: 69d44ea88b34aba027933cb3015a203bf06070fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297363"
---
# <span data-ttu-id="e4c37-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="e4c37-101">Set-AzDataShare</span></span>

## <span data-ttu-id="e4c37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4c37-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c37-103">Aktualisiert eine vorhandene Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="e4c37-103">Updates an existing data share</span></span>

## <span data-ttu-id="e4c37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4c37-104">SYNTAX</span></span>

### <span data-ttu-id="e4c37-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4c37-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4c37-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4c37-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4c37-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4c37-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4c37-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4c37-108">DESCRIPTION</span></span>
<span data-ttu-id="e4c37-109">Das Cmdlet " **Satz-AzDataShare** " aktualisiert eine Datenfreigabe, die innerhalb eines angegebenen Azure Data Share-Kontos vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e4c37-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="e4c37-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4c37-110">EXAMPLES</span></span>

### <span data-ttu-id="e4c37-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e4c37-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="e4c37-112">Mit diesem Befehl wird eine vorhandene Datenfreigabe mit dem Namen AdsShare aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e4c37-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="e4c37-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4c37-113">PARAMETERS</span></span>

### <span data-ttu-id="e4c37-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="e4c37-114">-AccountName</span></span>
<span data-ttu-id="e4c37-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="e4c37-115">Azure data share account name</span></span>

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

### <span data-ttu-id="e4c37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c37-116">-DefaultProfile</span></span>
<span data-ttu-id="e4c37-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e4c37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c37-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4c37-118">-Description</span></span>
<span data-ttu-id="e4c37-119">Beschreibung der Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="e4c37-119">Description of Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c37-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e4c37-120">-InputObject</span></span>
<span data-ttu-id="e4c37-121">Azure-Datenfreigabe Objekt</span><span class="sxs-lookup"><span data-stu-id="e4c37-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c37-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e4c37-122">-Name</span></span>
<span data-ttu-id="e4c37-123">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="e4c37-123">Azure data share name</span></span>

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

### <span data-ttu-id="e4c37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c37-124">-ResourceGroupName</span></span>
<span data-ttu-id="e4c37-125">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="e4c37-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e4c37-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e4c37-126">-ResourceId</span></span>
<span data-ttu-id="e4c37-127">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="e4c37-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="e4c37-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="e4c37-128">-TermsOfUse</span></span>
<span data-ttu-id="e4c37-129">Nutzungsbestimmungen für Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="e4c37-129">Terms of Use for Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c37-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e4c37-130">-Confirm</span></span>
<span data-ttu-id="e4c37-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4c37-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c37-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c37-132">-WhatIf</span></span>
<span data-ttu-id="e4c37-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4c37-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4c37-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4c37-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c37-135">CommonParameters</span></span>
<span data-ttu-id="e4c37-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c37-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4c37-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c37-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4c37-138">INPUTS</span></span>

### <span data-ttu-id="e4c37-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e4c37-139">System.String</span></span>

### <span data-ttu-id="e4c37-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="e4c37-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="e4c37-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4c37-141">OUTPUTS</span></span>

### <span data-ttu-id="e4c37-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="e4c37-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="e4c37-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4c37-143">NOTES</span></span>

## <span data-ttu-id="e4c37-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4c37-144">RELATED LINKS</span></span>
