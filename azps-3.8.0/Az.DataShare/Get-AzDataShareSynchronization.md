---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: 194fcfddef0d85925bc08fb53fa7f5acf860e9ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846284"
---
# <span data-ttu-id="4d399-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="4d399-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="4d399-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d399-102">SYNOPSIS</span></span>
<span data-ttu-id="4d399-103">Ruft Informationen zur Synchronisierungseinstellung für eine Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="4d399-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="4d399-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d399-104">SYNTAX</span></span>

### <span data-ttu-id="4d399-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d399-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d399-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d399-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d399-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d399-107">DESCRIPTION</span></span>
<span data-ttu-id="4d399-108">Das Cmdlet " **Get-AzDataShareSynchronization** " enthält Informationen zu allen Synchronisierungseinstellungen, die in einer Freigabe unter einem Datenfreigabe Konto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4d399-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="4d399-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d399-109">EXAMPLES</span></span>

### <span data-ttu-id="4d399-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d399-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="4d399-111">Dieser Befehl bietet Informationen zu allen Synchronisierungseinstellungen, die in der Freigabe AdsShare in Datenfreigabe Konto WikiAds vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4d399-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="4d399-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d399-112">PARAMETERS</span></span>

### <span data-ttu-id="4d399-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="4d399-113">-AccountName</span></span>
<span data-ttu-id="4d399-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="4d399-114">Azure data share account name</span></span>

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

### <span data-ttu-id="4d399-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d399-115">-DefaultProfile</span></span>
<span data-ttu-id="4d399-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d399-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d399-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d399-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d399-118">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="4d399-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4d399-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4d399-119">-ResourceId</span></span>
<span data-ttu-id="4d399-120">Azure Data Share-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4d399-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="4d399-121">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="4d399-121">-ShareName</span></span>
<span data-ttu-id="4d399-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="4d399-122">Azure data share name</span></span>

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

### <span data-ttu-id="4d399-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d399-123">CommonParameters</span></span>
<span data-ttu-id="4d399-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d399-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d399-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d399-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d399-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d399-126">INPUTS</span></span>

### <span data-ttu-id="4d399-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4d399-127">System.String</span></span>

## <span data-ttu-id="4d399-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d399-128">OUTPUTS</span></span>

### <span data-ttu-id="4d399-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="4d399-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="4d399-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d399-130">NOTES</span></span>

## <span data-ttu-id="4d399-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d399-131">RELATED LINKS</span></span>
