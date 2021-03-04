---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: d2741b3eb10618b9bdbe2e97b14d176c2b3eab26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926888"
---
# <span data-ttu-id="6cdd9-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="6cdd9-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="6cdd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cdd9-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdd9-103">Ruft eine Liste der Sicherungstresor für Azure NetApp-Dateien (ANF) ab.</span><span class="sxs-lookup"><span data-stu-id="6cdd9-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="6cdd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cdd9-104">SYNTAX</span></span>

### <span data-ttu-id="6cdd9-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6cdd9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cdd9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cdd9-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cdd9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cdd9-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cdd9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cdd9-108">DESCRIPTION</span></span>
<span data-ttu-id="6cdd9-109">Das **Get-AzNetAppFilesVault-Cmdlet** ruft eine Liste mit einem ANF-Konten-Sicherungstresor ab.</span><span class="sxs-lookup"><span data-stu-id="6cdd9-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="6cdd9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6cdd9-110">EXAMPLES</span></span>

### <span data-ttu-id="6cdd9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6cdd9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="6cdd9-112">Dieser Befehl ruft eine Liste der Sicherungstresor für Azure NetappFiles (ANF)-Konto "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="6cdd9-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="6cdd9-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6cdd9-113">PARAMETERS</span></span>

### <span data-ttu-id="6cdd9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6cdd9-114">-AccountName</span></span>
<span data-ttu-id="6cdd9-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="6cdd9-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cdd9-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6cdd9-116">-AccountObject</span></span>
<span data-ttu-id="6cdd9-117">Das Konto für das neue Sicherungsobjekt</span><span class="sxs-lookup"><span data-stu-id="6cdd9-117">The account for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cdd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cdd9-118">-DefaultProfile</span></span>
<span data-ttu-id="6cdd9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6cdd9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cdd9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cdd9-120">-ResourceGroupName</span></span>
<span data-ttu-id="6cdd9-121">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="6cdd9-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="6cdd9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cdd9-122">-ResourceId</span></span>
<span data-ttu-id="6cdd9-123">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="6cdd9-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="6cdd9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdd9-124">CommonParameters</span></span>
<span data-ttu-id="6cdd9-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cdd9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdd9-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cdd9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdd9-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6cdd9-127">INPUTS</span></span>

### <span data-ttu-id="6cdd9-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6cdd9-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="6cdd9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6cdd9-129">System.String</span></span>

## <span data-ttu-id="6cdd9-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6cdd9-130">OUTPUTS</span></span>

### <span data-ttu-id="6cdd9-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6cdd9-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="6cdd9-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6cdd9-132">NOTES</span></span>

## <span data-ttu-id="6cdd9-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6cdd9-133">RELATED LINKS</span></span>
