---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 9741a150dd26e3fef513984fa4ae8b6a2e7c97b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926944"
---
# <span data-ttu-id="061b2-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="061b2-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="061b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="061b2-102">SYNOPSIS</span></span>
<span data-ttu-id="061b2-103">Ruft Details zu einem Azure NetApp Files (ANF)-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="061b2-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="061b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="061b2-104">SYNTAX</span></span>

### <span data-ttu-id="061b2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="061b2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="061b2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="061b2-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="061b2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="061b2-107">DESCRIPTION</span></span>
<span data-ttu-id="061b2-108">Das **Get-AzNetAppFilesAccount-Cmdlet** ruft Details zu einem ANF-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="061b2-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="061b2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="061b2-109">EXAMPLES</span></span>

### <span data-ttu-id="061b2-110">Beispiel 1: Erhalten eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="061b2-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="061b2-111">Dieser Befehl ruft das Konto mit dem Namen MyAnfAccount ab.</span><span class="sxs-lookup"><span data-stu-id="061b2-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="061b2-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="061b2-112">PARAMETERS</span></span>

### <span data-ttu-id="061b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="061b2-113">-DefaultProfile</span></span>
<span data-ttu-id="061b2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="061b2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="061b2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="061b2-115">-Name</span></span>
<span data-ttu-id="061b2-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="061b2-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="061b2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="061b2-117">-ResourceGroupName</span></span>
<span data-ttu-id="061b2-118">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="061b2-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="061b2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="061b2-119">-ResourceId</span></span>
<span data-ttu-id="061b2-120">Die Ressourcen-ID des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="061b2-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="061b2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="061b2-121">CommonParameters</span></span>
<span data-ttu-id="061b2-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="061b2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="061b2-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="061b2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="061b2-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="061b2-124">INPUTS</span></span>

### <span data-ttu-id="061b2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="061b2-125">System.String</span></span>

## <span data-ttu-id="061b2-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="061b2-126">OUTPUTS</span></span>

### <span data-ttu-id="061b2-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="061b2-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="061b2-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="061b2-128">NOTES</span></span>

## <span data-ttu-id="061b2-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="061b2-129">RELATED LINKS</span></span>
