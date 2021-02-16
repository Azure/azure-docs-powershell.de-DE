---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153348"
---
# <span data-ttu-id="e6b71-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="e6b71-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="e6b71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b71-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b71-103">Ruft Informationen zu DataShare-Konten ab.</span><span class="sxs-lookup"><span data-stu-id="e6b71-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="e6b71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6b71-104">SYNTAX</span></span>

### <span data-ttu-id="e6b71-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6b71-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b71-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b71-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6b71-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b71-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b71-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6b71-108">DESCRIPTION</span></span>
<span data-ttu-id="e6b71-109">Das **Cmdlet "Get-AzDataShareAccount"** ruft Informationen zu Datenfreigabekonten in einer Azure-Abonnement-/Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e6b71-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="e6b71-110">Wenn Sie den Namen eines Kontos angeben, ruft dieses Cmdlet Informationen zu diesem datshare-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="e6b71-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="e6b71-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenfreigabekonten in einer Azure-Abonnement-/Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e6b71-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="e6b71-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6b71-112">EXAMPLES</span></span>

### <span data-ttu-id="e6b71-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6b71-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="e6b71-114">Dieser Befehl zeigt Informationen zu allen Datenfreigabekonten im Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="e6b71-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="e6b71-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6b71-115">PARAMETERS</span></span>

### <span data-ttu-id="e6b71-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b71-116">-DefaultProfile</span></span>
<span data-ttu-id="e6b71-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6b71-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b71-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e6b71-118">-Name</span></span>
<span data-ttu-id="e6b71-119">Name des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="e6b71-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b71-120">-ResourceGroupName</span></span>
<span data-ttu-id="e6b71-121">Der Ressourcengruppenname des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="e6b71-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b71-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6b71-122">-ResourceId</span></span>
<span data-ttu-id="e6b71-123">Die Ressourcen-ID des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="e6b71-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="e6b71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b71-124">CommonParameters</span></span>
<span data-ttu-id="e6b71-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b71-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6b71-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b71-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6b71-127">INPUTS</span></span>

### <span data-ttu-id="e6b71-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e6b71-128">System.String</span></span>

## <span data-ttu-id="e6b71-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6b71-129">OUTPUTS</span></span>

### <span data-ttu-id="e6b71-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="e6b71-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="e6b71-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e6b71-131">NOTES</span></span>

## <span data-ttu-id="e6b71-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e6b71-132">RELATED LINKS</span></span>
