---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147241"
---
# <span data-ttu-id="8128a-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8128a-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="8128a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8128a-102">SYNOPSIS</span></span>
<span data-ttu-id="8128a-103">Löscht ein Azure NetApp Files (ANF)-Konto.</span><span class="sxs-lookup"><span data-stu-id="8128a-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="8128a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8128a-104">SYNTAX</span></span>

### <span data-ttu-id="8128a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8128a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8128a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8128a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8128a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8128a-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8128a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8128a-108">DESCRIPTION</span></span>
<span data-ttu-id="8128a-109">Das **Cmdlet "Remove-AzNetAppFilesAccount"** löscht ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="8128a-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="8128a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8128a-110">EXAMPLES</span></span>

### <span data-ttu-id="8128a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8128a-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="8128a-112">Mit diesem Befehl wird das ANF-Konto "MyAnfAccount" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8128a-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="8128a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8128a-113">PARAMETERS</span></span>

### <span data-ttu-id="8128a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8128a-114">-DefaultProfile</span></span>
<span data-ttu-id="8128a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8128a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8128a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8128a-116">-InputObject</span></span>
<span data-ttu-id="8128a-117">Das zu entfernende Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="8128a-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8128a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8128a-118">-Name</span></span>
<span data-ttu-id="8128a-119">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="8128a-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8128a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8128a-120">-PassThru</span></span>
<span data-ttu-id="8128a-121">Rückgabe, ob das angegebene Konto erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="8128a-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="8128a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8128a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8128a-123">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="8128a-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8128a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8128a-124">-ResourceId</span></span>
<span data-ttu-id="8128a-125">Die Ressourcen-ID des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="8128a-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="8128a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8128a-126">-Confirm</span></span>
<span data-ttu-id="8128a-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8128a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8128a-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8128a-128">-WhatIf</span></span>
<span data-ttu-id="8128a-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8128a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8128a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8128a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8128a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8128a-131">CommonParameters</span></span>
<span data-ttu-id="8128a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8128a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8128a-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8128a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8128a-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8128a-134">INPUTS</span></span>

### <span data-ttu-id="8128a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8128a-135">System.String</span></span>

### <span data-ttu-id="8128a-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8128a-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="8128a-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8128a-137">OUTPUTS</span></span>

### <span data-ttu-id="8128a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8128a-138">System.Boolean</span></span>

## <span data-ttu-id="8128a-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8128a-139">NOTES</span></span>

## <span data-ttu-id="8128a-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8128a-140">RELATED LINKS</span></span>
