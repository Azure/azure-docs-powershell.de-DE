---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: de0f71a91ec4445ae4be58e904e58eb3a97cb9a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845036"
---
# <span data-ttu-id="e8827-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e8827-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="e8827-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8827-102">SYNOPSIS</span></span>
<span data-ttu-id="e8827-103">Löscht ein Azure NetApp-Dateien (ANF)-Konto.</span><span class="sxs-lookup"><span data-stu-id="e8827-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="e8827-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8827-104">SYNTAX</span></span>

### <span data-ttu-id="e8827-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8827-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8827-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8827-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8827-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8827-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8827-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8827-108">DESCRIPTION</span></span>
<span data-ttu-id="e8827-109">Das Cmdlet **Remove-AzNetAppFilesAccount** löscht ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="e8827-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="e8827-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8827-110">EXAMPLES</span></span>

### <span data-ttu-id="e8827-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8827-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="e8827-112">Mit diesem Befehl wird das ANF-Konto "MyAnfAccount" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e8827-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="e8827-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8827-113">PARAMETERS</span></span>

### <span data-ttu-id="e8827-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8827-114">-DefaultProfile</span></span>
<span data-ttu-id="e8827-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8827-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8827-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8827-116">-InputObject</span></span>
<span data-ttu-id="e8827-117">Das zu entfernende Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="e8827-117">The account object to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8827-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e8827-118">-Name</span></span>
<span data-ttu-id="e8827-119">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="e8827-119">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8827-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8827-120">-PassThru</span></span>
<span data-ttu-id="e8827-121">Zurückgeben, ob das angegebene Konto erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="e8827-121">Return whether the specified account was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8827-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8827-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8827-123">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="e8827-123">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8827-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e8827-124">-ResourceId</span></span>
<span data-ttu-id="e8827-125">Die Ressourcen-ID des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="e8827-125">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8827-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8827-126">-Confirm</span></span>
<span data-ttu-id="e8827-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8827-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8827-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8827-128">-WhatIf</span></span>
<span data-ttu-id="e8827-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8827-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8827-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8827-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8827-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8827-131">CommonParameters</span></span>
<span data-ttu-id="e8827-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8827-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e8827-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8827-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8827-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8827-134">INPUTS</span></span>

### <span data-ttu-id="e8827-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e8827-135">System.String</span></span>

### <span data-ttu-id="e8827-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e8827-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e8827-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8827-137">OUTPUTS</span></span>

### <span data-ttu-id="e8827-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8827-138">System.Boolean</span></span>

## <span data-ttu-id="e8827-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8827-139">NOTES</span></span>

## <span data-ttu-id="e8827-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8827-140">RELATED LINKS</span></span>
