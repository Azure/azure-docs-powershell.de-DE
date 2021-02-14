---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154524"
---
# <span data-ttu-id="05f16-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="05f16-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="05f16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05f16-102">SYNOPSIS</span></span>
<span data-ttu-id="05f16-103">Ruft Details zu einer Azure NetApp Files (ANF) Active Directory-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="05f16-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="05f16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05f16-104">SYNTAX</span></span>

### <span data-ttu-id="05f16-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="05f16-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05f16-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05f16-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05f16-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05f16-107">DESCRIPTION</span></span>
<span data-ttu-id="05f16-108">Das **Cmdlet "Get-AzNetAppFilesActiveDirectory"** ruft Details zu einer Active Directory-Konfiguration für ANF-Konten ab.</span><span class="sxs-lookup"><span data-stu-id="05f16-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="05f16-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05f16-109">EXAMPLES</span></span>

### <span data-ttu-id="05f16-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05f16-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="05f16-111">Dieser Befehl ruft die Ad-Konfiguration namens "MyADConfigName" für das Azure NetApp Files (ANF)-Konto mit dem Namen "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="05f16-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="05f16-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05f16-112">PARAMETERS</span></span>

### <span data-ttu-id="05f16-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="05f16-113">-AccountName</span></span>
<span data-ttu-id="05f16-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="05f16-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="05f16-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="05f16-115">-AccountObject</span></span>
<span data-ttu-id="05f16-116">Das Konto für das neue Active Directory-Objekt</span><span class="sxs-lookup"><span data-stu-id="05f16-116">The Account for the new Active Directory object</span></span>

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

### <span data-ttu-id="05f16-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="05f16-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="05f16-118">Die ActiveDirectoryId des ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="05f16-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

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

### <span data-ttu-id="05f16-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f16-119">-DefaultProfile</span></span>
<span data-ttu-id="05f16-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05f16-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05f16-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f16-121">-ResourceGroupName</span></span>
<span data-ttu-id="05f16-122">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="05f16-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="05f16-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f16-123">CommonParameters</span></span>
<span data-ttu-id="05f16-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05f16-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f16-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05f16-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f16-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05f16-126">INPUTS</span></span>

### <span data-ttu-id="05f16-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="05f16-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="05f16-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05f16-128">OUTPUTS</span></span>

### <span data-ttu-id="05f16-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="05f16-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="05f16-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="05f16-130">NOTES</span></span>

## <span data-ttu-id="05f16-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="05f16-131">RELATED LINKS</span></span>
