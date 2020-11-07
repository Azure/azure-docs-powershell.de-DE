---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f59796a51ccd1f3e5e77442cde434ab803d0781
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660973"
---
# <span data-ttu-id="7c149-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7c149-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="7c149-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c149-102">SYNOPSIS</span></span>
<span data-ttu-id="7c149-103">Löscht ein Azure NetApp-Dateien (ANF)-Konto.</span><span class="sxs-lookup"><span data-stu-id="7c149-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="7c149-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c149-104">SYNTAX</span></span>

### <span data-ttu-id="7c149-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c149-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c149-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c149-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c149-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c149-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c149-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c149-108">DESCRIPTION</span></span>
<span data-ttu-id="7c149-109">Das Cmdlet **Remove-AzNetAppFilesAccount** löscht ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="7c149-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="7c149-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c149-110">EXAMPLES</span></span>

### <span data-ttu-id="7c149-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c149-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="7c149-112">Mit diesem Befehl wird das ANF-Konto "MyAnfAccount" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7c149-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="7c149-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c149-113">PARAMETERS</span></span>

### <span data-ttu-id="7c149-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c149-114">-DefaultProfile</span></span>
<span data-ttu-id="7c149-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c149-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c149-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c149-116">-InputObject</span></span>
<span data-ttu-id="7c149-117">Das zu entfernende Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="7c149-117">The account object to remove</span></span>

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

### <span data-ttu-id="7c149-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7c149-118">-Name</span></span>
<span data-ttu-id="7c149-119">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="7c149-119">The name of the ANF account</span></span>

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

### <span data-ttu-id="7c149-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c149-120">-PassThru</span></span>
<span data-ttu-id="7c149-121">Zurückgeben, ob das angegebene Konto erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="7c149-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="7c149-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c149-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c149-123">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="7c149-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7c149-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7c149-124">-ResourceId</span></span>
<span data-ttu-id="7c149-125">Die Ressourcen-ID des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="7c149-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="7c149-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c149-126">-Confirm</span></span>
<span data-ttu-id="7c149-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c149-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c149-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c149-128">-WhatIf</span></span>
<span data-ttu-id="7c149-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c149-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c149-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c149-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c149-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c149-131">CommonParameters</span></span>
<span data-ttu-id="7c149-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c149-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7c149-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c149-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c149-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c149-134">INPUTS</span></span>

### <span data-ttu-id="7c149-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7c149-135">System.String</span></span>

### <span data-ttu-id="7c149-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7c149-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="7c149-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c149-137">OUTPUTS</span></span>

### <span data-ttu-id="7c149-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c149-138">System.Boolean</span></span>

## <span data-ttu-id="7c149-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c149-139">NOTES</span></span>

## <span data-ttu-id="7c149-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c149-140">RELATED LINKS</span></span>
