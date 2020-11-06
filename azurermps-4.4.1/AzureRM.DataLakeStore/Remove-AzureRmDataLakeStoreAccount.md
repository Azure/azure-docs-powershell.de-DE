---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500858"
---
# <span data-ttu-id="dc5e9-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc5e9-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="dc5e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5e9-103">Löscht ein Data Lake Store-Konto dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc5e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc5e9-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc5e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc5e9-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5e9-106">Das Cmdlet **Remove-AzureRmDataLakeStoreAccount** löscht ein Data Lake Store-Konto dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="dc5e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc5e9-107">EXAMPLES</span></span>

### <span data-ttu-id="dc5e9-108">Beispiel 1: Entfernen eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="dc5e9-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="dc5e9-109">Mit diesem Befehl wird das Kontonamens ContosoADL aus dem Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="dc5e9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc5e9-110">PARAMETERS</span></span>

### <span data-ttu-id="dc5e9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="dc5e9-111">-Force</span></span>
<span data-ttu-id="dc5e9-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc5e9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dc5e9-113">-Name</span></span>
<span data-ttu-id="dc5e9-114">Gibt den Namen des zu entfernenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-114">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="dc5e9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc5e9-115">-PassThru</span></span>
<span data-ttu-id="dc5e9-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dc5e9-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc5e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc5e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="dc5e9-119">Gibt die Ressourcengruppe an, die das zu entfernende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-119">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="dc5e9-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc5e9-120">-Confirm</span></span>
<span data-ttu-id="dc5e9-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc5e9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc5e9-122">-WhatIf</span></span>
<span data-ttu-id="dc5e9-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc5e9-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc5e9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5e9-125">-DefaultProfile</span></span>
<span data-ttu-id="dc5e9-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5e9-127">CommonParameters</span></span>
<span data-ttu-id="dc5e9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5e9-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5e9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5e9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc5e9-130">INPUTS</span></span>

## <span data-ttu-id="dc5e9-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc5e9-131">OUTPUTS</span></span>

### <span data-ttu-id="dc5e9-132">bool</span><span class="sxs-lookup"><span data-stu-id="dc5e9-132">bool</span></span>
<span data-ttu-id="dc5e9-133">Wenn passthru angegeben ist, wird nach dem erfolgreichen Abschluss "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc5e9-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="dc5e9-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc5e9-134">NOTES</span></span>

## <span data-ttu-id="dc5e9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc5e9-135">RELATED LINKS</span></span>

[<span data-ttu-id="dc5e9-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc5e9-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="dc5e9-137">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc5e9-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="dc5e9-138">Satz-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc5e9-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="dc5e9-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc5e9-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


