---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458944"
---
# <span data-ttu-id="60dda-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="60dda-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="60dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60dda-102">SYNOPSIS</span></span>
<span data-ttu-id="60dda-103">Ruft Details zu einer Azure NetApp Files (ANF) Active Directory-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="60dda-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="60dda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60dda-104">SYNTAX</span></span>

### <span data-ttu-id="60dda-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="60dda-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60dda-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60dda-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60dda-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60dda-107">DESCRIPTION</span></span>
<span data-ttu-id="60dda-108">Das **Cmdlet "Get-AzNetAppFilesActiveDirectory"** ruft Details zur Active Directory-Konfiguration eines ANF-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="60dda-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="60dda-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60dda-109">EXAMPLES</span></span>

### <span data-ttu-id="60dda-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60dda-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="60dda-111">Dieser Befehl ruft die AD-Konfiguration namens "MyADConfigName" für das Azure NetApp Files (ANF)-Konto namens "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="60dda-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="60dda-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60dda-112">PARAMETERS</span></span>

### <span data-ttu-id="60dda-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="60dda-113">-AccountName</span></span>
<span data-ttu-id="60dda-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="60dda-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="60dda-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="60dda-115">-AccountObject</span></span>
<span data-ttu-id="60dda-116">Das Konto für das neue Active Directory-Objekt</span><span class="sxs-lookup"><span data-stu-id="60dda-116">The Account for the new Active Directory object</span></span>

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

### <span data-ttu-id="60dda-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="60dda-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="60dda-118">Die ActiveDirectoryId des ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="60dda-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

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

### <span data-ttu-id="60dda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60dda-119">-DefaultProfile</span></span>
<span data-ttu-id="60dda-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60dda-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60dda-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60dda-121">-ResourceGroupName</span></span>
<span data-ttu-id="60dda-122">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="60dda-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="60dda-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60dda-123">CommonParameters</span></span>
<span data-ttu-id="60dda-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60dda-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60dda-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60dda-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60dda-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60dda-126">INPUTS</span></span>

### <span data-ttu-id="60dda-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="60dda-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="60dda-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60dda-128">OUTPUTS</span></span>

### <span data-ttu-id="60dda-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="60dda-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="60dda-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="60dda-130">NOTES</span></span>

## <span data-ttu-id="60dda-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="60dda-131">RELATED LINKS</span></span>
