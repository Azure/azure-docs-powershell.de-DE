---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009169"
---
# <span data-ttu-id="75b0b-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="75b0b-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="75b0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="75b0b-103">Ruft Details zu einem Azure NetApp-Dateien (ANF)-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="75b0b-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="75b0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75b0b-104">SYNTAX</span></span>

### <span data-ttu-id="75b0b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="75b0b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75b0b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75b0b-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75b0b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75b0b-107">DESCRIPTION</span></span>
<span data-ttu-id="75b0b-108">Das Cmdlet " **Get-AzNetAppFilesAccount** " ruft Details zu einem ANF-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="75b0b-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="75b0b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75b0b-109">EXAMPLES</span></span>

### <span data-ttu-id="75b0b-110">Beispiel 1: Abrufen eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="75b0b-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="75b0b-111">Dieser Befehl ruft das Konto mit dem Namen MyAnfAccount ab.</span><span class="sxs-lookup"><span data-stu-id="75b0b-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="75b0b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="75b0b-112">PARAMETERS</span></span>

### <span data-ttu-id="75b0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b0b-113">-DefaultProfile</span></span>
<span data-ttu-id="75b0b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75b0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75b0b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="75b0b-115">-Name</span></span>
<span data-ttu-id="75b0b-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="75b0b-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="75b0b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b0b-117">-ResourceGroupName</span></span>
<span data-ttu-id="75b0b-118">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="75b0b-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="75b0b-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="75b0b-119">-ResourceId</span></span>
<span data-ttu-id="75b0b-120">Die Ressourcen-ID des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="75b0b-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="75b0b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b0b-121">CommonParameters</span></span>
<span data-ttu-id="75b0b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b0b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b0b-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75b0b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b0b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75b0b-124">INPUTS</span></span>

### <span data-ttu-id="75b0b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="75b0b-125">System.String</span></span>

## <span data-ttu-id="75b0b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75b0b-126">OUTPUTS</span></span>

### <span data-ttu-id="75b0b-127">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="75b0b-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="75b0b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="75b0b-128">NOTES</span></span>

## <span data-ttu-id="75b0b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75b0b-129">RELATED LINKS</span></span>
