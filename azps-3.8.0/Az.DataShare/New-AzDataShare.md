---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: f2a9f5f5689d4e0d7907df481e22c2d8864266ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996865"
---
# <span data-ttu-id="cbe0b-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="cbe0b-101">New-AzDataShare</span></span>

## <span data-ttu-id="cbe0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cbe0b-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe0b-103">Erstellt eine Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-103">Creates a azure data share.</span></span>

## <span data-ttu-id="cbe0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbe0b-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbe0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbe0b-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe0b-106">Das Cmdlet **New-AzDataShare** erstellt eine Datenfreigabe innerhalb eines angegebenen Azure-Datenfreigabe Kontos, indem Sie den Namen der Ressourcengruppe, den Namen des Kontos, den Freigabenamen und den Freigabetyp bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="cbe0b-107">Beschreibung und Nutzungsbedingungen sind optionale Parameter, die beim Erstellen der Datenfreigabe festgesetzt werden können.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="cbe0b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cbe0b-108">EXAMPLES</span></span>

### <span data-ttu-id="cbe0b-109">Beispiel 1: Erstellen einer Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="cbe0b-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="cbe0b-110">Dieser Befehl erstellt eine Datenfreigabe mit dem Namen AdsShare der Art CopyBased in Datenfreigabe Konto WikiAdsAccount unter Ressourcengruppen anzeigen mit Beschreibung und Nutzungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="cbe0b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbe0b-111">PARAMETERS</span></span>

### <span data-ttu-id="cbe0b-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="cbe0b-112">-AccountName</span></span>
<span data-ttu-id="cbe0b-113">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="cbe0b-113">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe0b-114">-DefaultProfile</span></span>
<span data-ttu-id="cbe0b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbe0b-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbe0b-116">-Description</span></span>
<span data-ttu-id="cbe0b-117">Beschreibung der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="cbe0b-117">Description of azure data share</span></span>

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

### <span data-ttu-id="cbe0b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cbe0b-118">-Name</span></span>
<span data-ttu-id="cbe0b-119">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="cbe0b-119">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe0b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe0b-120">-ResourceGroupName</span></span>
<span data-ttu-id="cbe0b-121">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="cbe0b-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe0b-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="cbe0b-122">-TermsOfUse</span></span>
<span data-ttu-id="cbe0b-123">Nutzungsbestimmungen für Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="cbe0b-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="cbe0b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cbe0b-124">-Confirm</span></span>
<span data-ttu-id="cbe0b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbe0b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbe0b-126">-WhatIf</span></span>
<span data-ttu-id="cbe0b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbe0b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbe0b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe0b-129">CommonParameters</span></span>
<span data-ttu-id="cbe0b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe0b-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbe0b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe0b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cbe0b-132">INPUTS</span></span>

### <span data-ttu-id="cbe0b-133">Keine</span><span class="sxs-lookup"><span data-stu-id="cbe0b-133">None</span></span>

## <span data-ttu-id="cbe0b-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cbe0b-134">OUTPUTS</span></span>

### <span data-ttu-id="cbe0b-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="cbe0b-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="cbe0b-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="cbe0b-136">NOTES</span></span>

## <span data-ttu-id="cbe0b-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cbe0b-137">RELATED LINKS</span></span>
