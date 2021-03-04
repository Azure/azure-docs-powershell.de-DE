---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7198e34e7e888c2e89fce6cb5293bfc46bf57b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926936"
---
# <span data-ttu-id="88e08-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="88e08-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="88e08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e08-102">SYNOPSIS</span></span>
<span data-ttu-id="88e08-103">Ruft Details einer Azure NetApp Files (ANF)-Active Directory-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="88e08-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="88e08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88e08-104">SYNTAX</span></span>

### <span data-ttu-id="88e08-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="88e08-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88e08-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88e08-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88e08-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88e08-107">DESCRIPTION</span></span>
<span data-ttu-id="88e08-108">Das **Get-AzNetAppFilesActiveDirectory-Cmdlet** ruft Details einer Active Directory-Konfiguration für ANF-Konten ab.</span><span class="sxs-lookup"><span data-stu-id="88e08-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="88e08-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88e08-109">EXAMPLES</span></span>

### <span data-ttu-id="88e08-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88e08-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="88e08-111">Dieser Befehl ruft die AD-Konfiguration mit dem Namen MyADConfigName für das Azure NetApp Files (ANF)-Konto mit dem Namen MyAnfAccount ab.</span><span class="sxs-lookup"><span data-stu-id="88e08-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="88e08-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="88e08-112">PARAMETERS</span></span>

### <span data-ttu-id="88e08-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="88e08-113">-AccountName</span></span>
<span data-ttu-id="88e08-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="88e08-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="88e08-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="88e08-115">-AccountObject</span></span>
<span data-ttu-id="88e08-116">Das Konto für das neue Active Directory-Objekt</span><span class="sxs-lookup"><span data-stu-id="88e08-116">The Account for the new Active Directory object</span></span>

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

### <span data-ttu-id="88e08-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="88e08-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="88e08-118">Die ActiveDirectoryId des ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="88e08-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e08-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e08-119">-DefaultProfile</span></span>
<span data-ttu-id="88e08-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88e08-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e08-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e08-121">-ResourceGroupName</span></span>
<span data-ttu-id="88e08-122">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="88e08-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="88e08-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e08-123">CommonParameters</span></span>
<span data-ttu-id="88e08-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e08-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e08-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88e08-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e08-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88e08-126">INPUTS</span></span>

### <span data-ttu-id="88e08-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="88e08-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="88e08-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88e08-128">OUTPUTS</span></span>

### <span data-ttu-id="88e08-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="88e08-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="88e08-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="88e08-130">NOTES</span></span>

## <span data-ttu-id="88e08-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="88e08-131">RELATED LINKS</span></span>
