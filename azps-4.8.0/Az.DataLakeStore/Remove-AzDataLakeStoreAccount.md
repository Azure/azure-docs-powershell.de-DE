---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175234"
---
# <span data-ttu-id="2d76f-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2d76f-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="2d76f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d76f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d76f-103">Löscht ein Data Lake Store-Konto dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="2d76f-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="2d76f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d76f-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d76f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d76f-105">DESCRIPTION</span></span>
<span data-ttu-id="2d76f-106">Das Cmdlet **Remove-AzDataLakeStoreAccount** löscht ein Data Lake Store-Konto dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="2d76f-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="2d76f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d76f-107">EXAMPLES</span></span>

### <span data-ttu-id="2d76f-108">Beispiel 1: Entfernen eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="2d76f-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="2d76f-109">Mit diesem Befehl wird das Kontonamens ContosoADL aus dem Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="2d76f-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="2d76f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d76f-110">PARAMETERS</span></span>

### <span data-ttu-id="2d76f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d76f-111">-DefaultProfile</span></span>
<span data-ttu-id="2d76f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2d76f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d76f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2d76f-113">-Force</span></span>
<span data-ttu-id="2d76f-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2d76f-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d76f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2d76f-115">-Name</span></span>
<span data-ttu-id="2d76f-116">Gibt den Namen des zu entfernenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="2d76f-116">Specifies the name of the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d76f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d76f-117">-PassThru</span></span>
<span data-ttu-id="2d76f-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2d76f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2d76f-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2d76f-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d76f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d76f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d76f-121">Gibt die Ressourcengruppe an, die das zu entfernende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="2d76f-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d76f-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d76f-122">-Confirm</span></span>
<span data-ttu-id="2d76f-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d76f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d76f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d76f-124">-WhatIf</span></span>
<span data-ttu-id="2d76f-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d76f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d76f-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d76f-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d76f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d76f-127">CommonParameters</span></span>
<span data-ttu-id="2d76f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d76f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d76f-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d76f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d76f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d76f-130">INPUTS</span></span>

### <span data-ttu-id="2d76f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2d76f-131">System.String</span></span>

## <span data-ttu-id="2d76f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d76f-132">OUTPUTS</span></span>

### <span data-ttu-id="2d76f-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d76f-133">System.Boolean</span></span>

## <span data-ttu-id="2d76f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d76f-134">NOTES</span></span>

## <span data-ttu-id="2d76f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d76f-135">RELATED LINKS</span></span>

[<span data-ttu-id="2d76f-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2d76f-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="2d76f-137">Neu – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2d76f-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="2d76f-138">Satz-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2d76f-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="2d76f-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2d76f-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


