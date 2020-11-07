---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: 2b3eda3aadca93415d93154a9a70361c789c94ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845443"
---
# <span data-ttu-id="71d34-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="71d34-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="71d34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71d34-102">SYNOPSIS</span></span>
<span data-ttu-id="71d34-103">Erstellt ein neues Konto für Datenfreigaben</span><span class="sxs-lookup"><span data-stu-id="71d34-103">Creates new data share account</span></span>

## <span data-ttu-id="71d34-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71d34-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71d34-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71d34-105">DESCRIPTION</span></span>
<span data-ttu-id="71d34-106">Cmdlet **New-AzDataShareAccount** erstellt ein DataShare-Konto in der angegebenen Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71d34-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="71d34-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71d34-107">EXAMPLES</span></span>

### <span data-ttu-id="71d34-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71d34-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="71d34-109">Erstellt in der Ressourcengruppe "anzeigen" ein Konto mit dem Namen "WikiADS"</span><span class="sxs-lookup"><span data-stu-id="71d34-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="71d34-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="71d34-110">PARAMETERS</span></span>

### <span data-ttu-id="71d34-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71d34-111">-AsJob</span></span>
<span data-ttu-id="71d34-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="71d34-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="71d34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d34-113">-DefaultProfile</span></span>
<span data-ttu-id="71d34-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71d34-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71d34-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="71d34-115">-Location</span></span>
<span data-ttu-id="71d34-116">Der Speicherort, an dem das Datenfreigabe Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71d34-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="71d34-117">-Name</span><span class="sxs-lookup"><span data-stu-id="71d34-117">-Name</span></span>
<span data-ttu-id="71d34-118">Name des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="71d34-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="71d34-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d34-119">-ResourceGroupName</span></span>
<span data-ttu-id="71d34-120">Der Ressourcengruppenname des Azure Data Share-Kontos wird in erstellt.</span><span class="sxs-lookup"><span data-stu-id="71d34-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="71d34-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="71d34-121">-Tag</span></span>
<span data-ttu-id="71d34-122">Die Tags, die dem Azure-Datenfreigabe Konto zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71d34-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d34-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71d34-123">-Confirm</span></span>
<span data-ttu-id="71d34-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71d34-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71d34-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71d34-125">-WhatIf</span></span>
<span data-ttu-id="71d34-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71d34-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71d34-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71d34-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71d34-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d34-128">CommonParameters</span></span>
<span data-ttu-id="71d34-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d34-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d34-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d34-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d34-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71d34-131">INPUTS</span></span>

### <span data-ttu-id="71d34-132">Keine</span><span class="sxs-lookup"><span data-stu-id="71d34-132">None</span></span>

## <span data-ttu-id="71d34-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71d34-133">OUTPUTS</span></span>

### <span data-ttu-id="71d34-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="71d34-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="71d34-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="71d34-135">NOTES</span></span>

## <span data-ttu-id="71d34-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71d34-136">RELATED LINKS</span></span>
